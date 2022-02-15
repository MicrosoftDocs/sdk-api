---
UID: NF:d2d1.ID2D1RenderTarget.BeginDraw
title: ID2D1RenderTarget::BeginDraw (d2d1.h)
description: Initiates drawing on this render target.
helpviewer_keywords: ["BeginDraw","BeginDraw method [Direct2D]","BeginDraw method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","BeginDraw method","ID2D1RenderTarget.BeginDraw","ID2D1RenderTarget::BeginDraw","d2d1/ID2D1RenderTarget::BeginDraw","direct2d.ID2D1RenderTarget_BeginDraw"]
old-location: direct2d\ID2D1RenderTarget_BeginDraw.htm
tech.root: Direct2D
ms.assetid: 0562b286-7427-4d76-b699-a39356496a0f
ms.date: 12/05/2018
ms.keywords: BeginDraw, BeginDraw method [Direct2D], BeginDraw method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],BeginDraw method, ID2D1RenderTarget.BeginDraw, ID2D1RenderTarget::BeginDraw, d2d1/ID2D1RenderTarget::BeginDraw, direct2d.ID2D1RenderTarget_BeginDraw
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
 - ID2D1RenderTarget::BeginDraw
 - d2d1/ID2D1RenderTarget::BeginDraw
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
 - ID2D1RenderTarget.BeginDraw
---

# ID2D1RenderTarget::BeginDraw


## -description

Initiates drawing on this render target.



## -remarks

Drawing operations can only be issued between a <b>BeginDraw</b> and <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> call.

BeginDraw and EndDraw are used to indicate that a render target is in use by the Direct2D system. Different implementations of <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a> might behave differently when <b>BeginDraw</b> is called. An <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a> may be locked between <b>BeginDraw</b>/<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> calls, a DXGI surface render target might be acquired on <b>BeginDraw</b> and released on <b>EndDraw</b>, while an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> may begin batching at <b>BeginDraw</b> and may present on <b>EndDraw</b>, for example.

The BeginDraw method must be called before rendering operations can be called, though state-setting and state-retrieval operations can be performed even outside of <b>BeginDraw</b>/<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a>. 

After <b>BeginDraw</b> is called, a render target will normally build up a batch of rendering commands, but defer processing of these commands until either an internal buffer is full, the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a> method is called, or until <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> is called. The <b>EndDraw</b> method causes any batched drawing operations to complete, and then returns an HRESULT indicating the success of the operations and, optionally, the tag state of the render target at the time the error occurred. The <b>EndDraw</b> method always succeeds: it should not be called twice even if a previous <b>EndDraw</b> resulted in a failing HRESULT. 

If <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw">EndDraw</a> is called without a matched call to <b>BeginDraw</b>, it returns an error indicating that <b>BeginDraw</b> must be called before <b>EndDraw</b>.

Calling <b>BeginDraw</b> twice on a render target puts the target into an error state where nothing further is drawn, and returns an appropriate HRESULT and error information when <b>EndDraw</b> is called.



## Examples

The following example uses an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> to draw text to a window.


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

## -see-also

<a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a>

