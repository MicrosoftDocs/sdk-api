---
UID: NF:d2d1.ID2D1RenderTarget.EndDraw
title: ID2D1RenderTarget::EndDraw (d2d1.h)
description: Ends drawing operations on the render target and indicates the current error state and associated tags.
helpviewer_keywords: ["EndDraw","EndDraw method [Direct2D]","EndDraw method [Direct2D]","ID2D1RenderTarget interface","ID2D1RenderTarget interface [Direct2D]","EndDraw method","ID2D1RenderTarget.EndDraw","ID2D1RenderTarget::EndDraw","d2d1/ID2D1RenderTarget::EndDraw","direct2d.ID2D1RenderTarget_EndDraw"]
old-location: direct2d\ID2D1RenderTarget_EndDraw.htm
tech.root: Direct2D
ms.assetid: a8f24501-4e85-4981-bb38-2bd6333a7b49
ms.date: 12/05/2018
ms.keywords: EndDraw, EndDraw method [Direct2D], EndDraw method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],EndDraw method, ID2D1RenderTarget.EndDraw, ID2D1RenderTarget::EndDraw, d2d1/ID2D1RenderTarget::EndDraw, direct2d.ID2D1RenderTarget_EndDraw
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
 - ID2D1RenderTarget::EndDraw
 - d2d1/ID2D1RenderTarget::EndDraw
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
 - ID2D1RenderTarget.EndDraw
---

# ID2D1RenderTarget::EndDraw


## -description

Ends drawing operations  on the render target and indicates the current error state and associated tags.

## -parameters

### -param tag1 [out, optional]

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

When this method returns, contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.

### -param tag2 [out, optional]

Type: <b><a href="/windows/win32/Direct2D/d2d1-tag">D2D1_TAG</a>*</b>

When this method returns, contains the tag for drawing operations that caused errors or 0 if there were no errors. This parameter is passed uninitialized.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code and sets <i>tag1</i> and <i>tag2</i> to the tags that were active when the error occurred.

## -remarks

Drawing operations can only be issued between a <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a> and <b>EndDraw</b> call.


<a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a> and <b>EndDraw</b> are use to indicate that a render target is in use by the Direct2D system. Different implementations of <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget">ID2D1RenderTarget</a> might behave differently when <b>BeginDraw</b> is called. An <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1bitmaprendertarget">ID2D1BitmapRenderTarget</a> may be locked between <b>BeginDraw</b>/<b>EndDraw</b> calls, a DXGI surface render target might be acquired on <b>BeginDraw</b> and released on <b>EndDraw</b>, while an <a href="/windows/win32/api/d2d1/nn-d2d1-id2d1hwndrendertarget">ID2D1HwndRenderTarget</a> may begin batching at <b>BeginDraw</b> and may present on <b>EndDraw</b>, for example.

The <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a> method must be called before rendering operations can be called, though state-setting and state-retrieval operations can be performed even outside of <b>BeginDraw</b>/<b>EndDraw</b>. 

After <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a> is called, a render target will normally build up a batch of rendering commands, but defer processing of these commands until either an internal buffer is full, the <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush">Flush</a> method is called, or until <b>EndDraw</b> is called. The <b>EndDraw</b> method causes any batched drawing operations to complete, and then returns an <b>HRESULT</b> indicating the success of the operations and, optionally, the tag state of the render target at the time the error occurred. The <b>EndDraw</b> method always succeeds: it should not be called twice even if a previous <b>EndDraw</b> resulted in a failing <b>HRESULT</b>. 

If <b>EndDraw</b> is called without a matched call to <a href="/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw">BeginDraw</a>, it returns an error indicating that <b>BeginDraw</b> must be called before <b>EndDraw</b>.

Calling <b>BeginDraw</b> twice on a render target puts the target into an error state where nothing further is drawn, and returns an appropriate <b>HRESULT</b> and error information when <b>EndDraw</b> is called.



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

