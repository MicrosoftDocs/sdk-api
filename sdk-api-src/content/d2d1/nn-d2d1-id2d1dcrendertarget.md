---
UID: NN:d2d1.ID2D1DCRenderTarget
title: ID2D1DCRenderTarget (d2d1.h)
description: Issues drawing commands to a GDI device context.
helpviewer_keywords: ["ID2D1DCRenderTarget","ID2D1DCRenderTarget interface [Direct2D]","ID2D1DCRenderTarget interface [Direct2D]","described","d2d1/ID2D1DCRenderTarget","direct2d.ID2D1DCRenderTarget"]
old-location: direct2d\ID2D1DCRenderTarget.htm
tech.root: Direct2D
ms.assetid: 6546998e-6740-413a-88c5-36fa0decec8f
ms.date: 12/05/2018
ms.keywords: ID2D1DCRenderTarget, ID2D1DCRenderTarget interface [Direct2D], ID2D1DCRenderTarget interface [Direct2D],described, d2d1/ID2D1DCRenderTarget, direct2d.ID2D1DCRenderTarget
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1DCRenderTarget
 - d2d1/ID2D1DCRenderTarget
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DCRenderTarget
---

# ID2D1DCRenderTarget interface


## -description

Issues drawing commands to a GDI device context.

## -inheritance

The <b>ID2D1DCRenderTarget</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>. <b>ID2D1DCRenderTarget</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

<h3><a id="Creating_ID2D1DCRenderTarget_Objects"></a><a id="creating_id2d1dcrendertarget_objects"></a><a id="CREATING_ID2D1DCRENDERTARGET_OBJECTS"></a>Creating ID2D1DCRenderTarget Objects</h3>
To create an <b>ID2D1DCRenderTarget</b>, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createdcrendertarget">ID2D1Factory::CreateDCRenderTarget</a> method.

Before you can render with the DC render target, you must use its <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc">BindDC</a> method to associate it with a GDI DC.  You do this each time you  use a different DC, or the size of the area you want to draw to changes.

To enable the DC render target to work with GDI, set its pixel format to <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a> and its alpha mode to <a href="/windows/win32/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_PREMULTIPLIED</a> or <b>D2D1_ALPHA_MODE_IGNORE</b>.

Your application should create render targets once and hold onto them for the life of the application or until the render target's  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> method returns the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created).

<h3><a id="ID2D1DCRenderTargets__GDI_Transforms__and_Right-to-Left_Language_Builds_of_Windows"></a><a id="id2d1dcrendertargets__gdi_transforms__and_right-to-left_language_builds_of_windows"></a><a id="ID2D1DCRENDERTARGETS__GDI_TRANSFORMS__AND_RIGHT-TO-LEFT_LANGUAGE_BUILDS_OF_WINDOWS"></a>ID2D1DCRenderTargets, GDI Transforms, and Right-to-Left Language Builds of Windows</h3>
When you use an <b>ID2D1DCRenderTarget</b>, it renders Direct2D content to an internal bitmap, and then renders the bitmap to the DC with GDI. 

It's possible for GDI to apply a GDI transform  (through the <a href="/windows/win32/api/wingdi/nf-wingdi-setworldtransform">SetWorldTransform</a> method) or other effect to the same DC used by the render target, in which case GDI transforms the bitmap produced by Direct2D. Using a GDI transform to transform the Direct2D content has the potential to degrade the visual quality of the output, because you're transforming a bitmap for which antialiasing and subpixel positioning have already been calculated.

For example, suppose you use the render target to draw a scene that contains antialiased geometries and text. If you use a GDI transform to apply a scale transform to the DC and scale the scene so that it's 10 times larger, you'll see pixelization and jagged edges. (If, however, you applied a similar transform using Direct2D, the visual quality of the scene would not be degraded.)

In some cases, it might not be obvious that GDI is performing additional processing that might degrade the quality of the Direct2D content. For example, on a right-to-left (RTL) build of Windows, content rendered by an <b>ID2D1DCRenderTarget</b> might be horizontally inverted when GDI copies it to its destination.   Whether the content is actually inverted depends on the current settings of the DC.

Depending on the type of content being rendered, you might want to prevent the inversion. If the Direct2D content includes ClearType text, this inversion will degrade the quality of the text.

You can control RTL rendering behavior by using the <a href="/windows/win32/api/wingdi/nf-wingdi-setlayout">SetLayout</a> GDI function.  To  prevent the mirroring, call the <b>SetLayout</b> GDI function and specify <b>LAYOUT_BITMAPORIENTATIONPRESERVED</b> as the only value for the second parameter (do not combine it with <b>LAYOUT_RTL</b>), as shown in the following example:


```cpp
SetLayout(m_hwnd, LAYOUT_BITMAPORIENTATIONPRESERVED);
```



## Examples

The following code creates a DC render target.


```cpp
// Create a DC render target.
D2D1_RENDER_TARGET_PROPERTIES props = D2D1::RenderTargetProperties(
    D2D1_RENDER_TARGET_TYPE_DEFAULT,
    D2D1::PixelFormat(
        DXGI_FORMAT_B8G8R8A8_UNORM,
        D2D1_ALPHA_MODE_IGNORE),
    0,
    0,
    D2D1_RENDER_TARGET_USAGE_NONE,
    D2D1_FEATURE_LEVEL_DEFAULT
    );

hr = m_pD2DFactory->CreateDCRenderTarget(&props, &m_pDCRT);

```


In the preceding code, <i>m_pD2DFactory</i> is a  pointer to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>, and <i>m_pDCRT</i> is a pointer to an <b>ID2D1DCRenderTarget</b>. 

The next code example binds a DC to the <b>ID2D1DCRenderTarget</b>.


```cpp
HRESULT DemoApp::OnRender(const PAINTSTRUCT &ps)
{

```

```cpp
// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &rc);

```

```cpp
// Bind the DC to the DC render target.
hr = m_pDCRT->BindDC(ps.hdc, &rc);

```


For more information about using GDI with Direct2D, see the <a href="/windows/win32/Direct2D/direct2d-and-gdi-interoperation-overview">Direct2D and GDI Interoperation Overview</a>.

<div class="code"></div>

## -see-also

<a href="/windows/win32/Direct2D/direct2d-and-gdi-interoperation-overview">Direct2D and GDI Interoperation Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

