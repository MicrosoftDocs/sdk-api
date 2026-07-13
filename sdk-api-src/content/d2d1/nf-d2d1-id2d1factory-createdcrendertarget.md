---
UID: NF:d2d1.ID2D1Factory.CreateDCRenderTarget
title: ID2D1Factory::CreateDCRenderTarget (d2d1.h)
description: Creates a render target that draws to a Windows Graphics Device Interface (GDI) device context.
helpviewer_keywords: ["CreateDCRenderTarget","CreateDCRenderTarget method [Direct2D]","CreateDCRenderTarget method [Direct2D]","ID2D1Factory interface","ID2D1Factory interface [Direct2D]","CreateDCRenderTarget method","ID2D1Factory.CreateDCRenderTarget","ID2D1Factory::CreateDCRenderTarget","d2d1/ID2D1Factory::CreateDCRenderTarget","direct2d.ID2D1Factory_CreateDCRenderTarget"]
old-location: direct2d\ID2D1Factory_CreateDCRenderTarget.htm
tech.root: Direct2D
ms.assetid: de062068-d2b5-4576-a475-a0e2c9840506
ms.date: 12/05/2018
ms.keywords: CreateDCRenderTarget, CreateDCRenderTarget method [Direct2D], CreateDCRenderTarget method [Direct2D],ID2D1Factory interface, ID2D1Factory interface [Direct2D],CreateDCRenderTarget method, ID2D1Factory.CreateDCRenderTarget, ID2D1Factory::CreateDCRenderTarget, d2d1/ID2D1Factory::CreateDCRenderTarget, direct2d.ID2D1Factory_CreateDCRenderTarget
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
 - ID2D1Factory::CreateDCRenderTarget
 - d2d1/ID2D1Factory::CreateDCRenderTarget
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
 - ID2D1Factory.CreateDCRenderTarget
---

# ID2D1Factory::CreateDCRenderTarget


## -description

Creates a render target that draws to a Windows Graphics Device Interface (GDI) device context.

## -parameters

### -param renderTargetProperties [in]

Type: <b>const <a href="/windows/win32/api/d2d1/ns-d2d1-d2d1_render_target_properties">D2D1_RENDER_TARGET_PROPERTIES</a>*</b>

The rendering mode, pixel format, remoting options, DPI information, and the minimum DirectX support required for hardware rendering.  To enable the device context (DC) render target to work with GDI, set the DXGI format to <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a> and the alpha mode to <a href="/windows/win32/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_PREMULTIPLIED</a> or <b>D2D1_ALPHA_MODE_IGNORE</b>. For more information about pixel formats, see  <a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel  Formats and Alpha Modes</a>.

### -param dcRenderTarget [out]

Type: <b><a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a>**</b>

When this method returns, <i>dcRenderTarget</i> contains the address of the pointer to the  <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a> created by the method.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an [**HRESULT**](/windows/desktop/com/structure-of-com-error-codes) error code.

## -remarks

Before you can render with a DC render target, you must use the render target's <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1dcrendertarget-binddc">BindDC</a> method to associate it with a GDI DC.  Do this for each different DC and whenever there is a change in the size of the area you want to draw to.

To enable the DC render target to work with GDI, set the render target's DXGI format to <a href="/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_B8G8R8A8_UNORM</a> and alpha mode to <a href="/windows/win32/api/dcommon/ne-dcommon-d2d1_alpha_mode">D2D1_ALPHA_MODE_PREMULTIPLIED</a> or <b>D2D1_ALPHA_MODE_IGNORE</b>.

Your application should create render targets once and hold on to them for the life of the application or until the render target's  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> method returns the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, recreate the render target (and any resources it created).


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


In the preceding code, <i>m_pD2DFactory</i> is a  pointer to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>, and <i>m_pDCRT</i> is a pointer to an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a>. 

The next code example binds a DC to the <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1dcrendertarget">ID2D1DCRenderTarget</a>.


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

## -see-also

<a href="/windows/win32/Direct2D/direct2d-and-gdi-interoperation-overview">Direct2D and GDI Interoperation Overview</a>



<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1factory">ID2D1Factory</a>



<a href="/windows/win32/Direct2D/supported-pixel-formats-and-alpha-modes">Supported Pixel  Formats and Alpha Modes</a>

