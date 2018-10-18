---
UID: NF:d2d1.ID2D1RenderTarget.BeginDraw
title: ID2D1RenderTarget::BeginDraw
author: windows-sdk-content
description: Initiates drawing on this render target.
old-location: direct2d\ID2D1RenderTarget_BeginDraw.htm
tech.root: direct2d
ms.assetid: 0562b286-7427-4d76-b699-a39356496a0f
ms.author: windowssdkdev
ms.date: 10/17/2018
ms.keywords: BeginDraw, BeginDraw method [Direct2D], BeginDraw method [Direct2D],ID2D1RenderTarget interface, ID2D1RenderTarget interface [Direct2D],BeginDraw method, ID2D1RenderTarget.BeginDraw, ID2D1RenderTarget::BeginDraw, d2d1/ID2D1RenderTarget::BeginDraw, direct2d.ID2D1RenderTarget_BeginDraw
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1RenderTarget.BeginDraw
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1RenderTarget::BeginDraw


## -description


Initiates drawing on this render target. 


## -parameters






## -returns



This method does not return a value.




## -remarks



Drawing operations can only be issued between a <b>BeginDraw</b> and <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> call.

BeginDraw and EndDraw are used to indicate that a render target is in use by the Direct2D system. Different implementations of <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a> might behave differently when <b>BeginDraw</b> is called. An <a href="https://msdn.microsoft.com/f298d4f7-acb8-4fbe-89f7-2410e3b753bd">ID2D1BitmapRenderTarget</a> may be locked between <b>BeginDraw</b>/<a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> calls, a DXGI surface render target might be acquired on <b>BeginDraw</b> and released on <b>EndDraw</b>, while an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a> may begin batching at <b>BeginDraw</b> and may present on <b>EndDraw</b>, for example.

The BeginDraw method must be called before rendering operations can be called, though state-setting and state-retrieval operations can be performed even outside of <b>BeginDraw</b>/<a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a>. 

After <b>BeginDraw</b> is called, a render target will normally build up a batch of rendering commands, but defer processing of these commands until either an internal buffer is full, the <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a> method is called, or until <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> is called. The <b>EndDraw</b> method causes any batched drawing operations to complete, and then returns an HRESULT indicating the success of the operations and, optionally, the tag state of the render target at the time the error occurred. The <b>EndDraw</b> method always succeeds: it should not be called twice even if a previous <b>EndDraw</b> resulted in a failing HRESULT. 

If <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> is called without a matched call to <b>BeginDraw</b>, it returns an error indicating that <b>BeginDraw</b> must be called before <b>EndDraw</b>.

Calling <b>BeginDraw</b> twice on a render target puts the target into an error state where nothing further is drawn, and returns an appropriate HRESULT and error information when <b>EndDraw</b> is called.



#### Examples

The following example uses an <a href="https://msdn.microsoft.com/860342cc-989c-4432-b879-07f3da07d50a">ID2D1HwndRenderTarget</a> to draw text to a window.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//  Called whenever the application needs to display the client
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
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget-&gt;GetSize();

        m_pRenderTarget-&gt;BeginDraw();

        m_pRenderTarget-&gt;SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget-&gt;Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget-&gt;DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget-&gt;EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

