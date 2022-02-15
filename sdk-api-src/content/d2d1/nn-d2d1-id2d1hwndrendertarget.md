---
UID: NN:d2d1.ID2D1HwndRenderTarget
title: ID2D1HwndRenderTarget (d2d1.h)
description: Renders drawing instructions to a window.
helpviewer_keywords: ["ID2D1HwndRenderTarget","ID2D1HwndRenderTarget interface [Direct2D]","ID2D1HwndRenderTarget interface [Direct2D]","described","d2d1/ID2D1HwndRenderTarget","direct2d.ID2D1HwndRenderTarget"]
old-location: direct2d\ID2D1HwndRenderTarget.htm
tech.root: Direct2D
ms.assetid: 860342cc-989c-4432-b879-07f3da07d50a
ms.date: 12/05/2018
ms.keywords: ID2D1HwndRenderTarget, ID2D1HwndRenderTarget interface [Direct2D], ID2D1HwndRenderTarget interface [Direct2D],described, d2d1/ID2D1HwndRenderTarget, direct2d.ID2D1HwndRenderTarget
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
 - ID2D1HwndRenderTarget
 - d2d1/ID2D1HwndRenderTarget
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
 - ID2D1HwndRenderTarget
---

# ID2D1HwndRenderTarget interface


## -description

Renders drawing instructions to a window.

## -inheritance

The <b>ID2D1HwndRenderTarget</b> interface inherits from <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>. <b>ID2D1HwndRenderTarget</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

As is the case with other render targets, you must call <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a>  before issuing drawing commands. After you've finished drawing, call <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> to indicate that drawing is finished and to release access to the buffer backing the render target.

For <b>ID2D1HwndRenderTarget</b>, the only side effect of <b>BeginDraw</b> is changing the state of the render target to allow drawing commands to be issued.

<b>EndDraw</b> flushes any batched drawing commands. If no errors have occurred, then it also presents the buffer, causing it to appear on the associated window. Finally, <b>EndDraw</b> returns the HRESULT of the first error that occurred in drawing or presenting, as well as the tag state at the time the error occurred.

<b>ID2D1HwndRenderTarget</b> objects are double buffered, so drawing commands issued do not appear immediately, but rather are performed on an offscreen surface. When <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> is called, if there have been no rendering errors, the offscreen buffer is presented. If there have been rendering errors in the batch flushed by <b>EndDraw</b>, then the buffer is not presented, and the application must call <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a> and re-draw the frame. <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a> can be used to check for errors before calling <b>EndDraw</b> if an application wants the frame to be presented regardless of errors.



A hardware render target's back-buffer is the size specified by <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1hwndrendertarget-resize(constd2d1_size_u)">GetPixelSize</a>. If <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> presents the buffer, this bitmap is stretched to cover the surface where it is presented: the entire client area of the window. This stretch is performed using bilinear filtering if the render target is rendering in hardware and using nearest-neighbor filtering if the rendering target is using software. (Typically, an application will call Resize to ensure the pixel size of the render target and the pixel size of the destination match, and no scaling is necessary, though this is not a requirement.)



In the case where a window straddles adapters, Direct2D ensures that the portion of the off-screen render target is copied from the adapter where rendering is occurring to the adapter that needs to display the contents.



If the adapter a render target is on has been removed or the driver upgraded while the application is running, this is returned as an error in the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> call. In this case, the application should create a new render target and resources as necessary.


<h3><a id="Creating_ID2D1HwndRenderTarget_Objects"></a><a id="creating_id2d1hwndrendertarget_objects"></a><a id="CREATING_ID2D1HWNDRENDERTARGET_OBJECTS"></a>Creating ID2D1HwndRenderTarget Objects</h3>
To create an <b>ID2D1HwndRenderTarget</b>, use the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties_constd2d1_hwnd_render_target_properties_id2d1hwndrendertarget)">ID2D1Factory::CreateHwndRenderTarget</a> method.

Your application should create render targets once and hold onto them for the life of the application or until the render target's  <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> method returns the <a href="/windows/win32/Direct2D/direct2d-error-codes">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created).


## Examples

The following example uses the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties_constd2d1_hwnd_render_target_properties_id2d1hwndrendertarget)">CreateHwndRenderTarget</a> method to create an <b>ID2D1HwndRenderTarget</b>.


```cpp
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );

```


The next example uses the <b>ID2D1HwndRenderTarget</b> to draw text to the window.


```cpp
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}

```


Code has been omitted from this example.

<div class="code"></div>

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

