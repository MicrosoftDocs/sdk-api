---
UID: NN:d2d1.ID2D1HwndRenderTarget
title: ID2D1HwndRenderTarget
author: windows-sdk-content
description: Renders drawing instructions to a window.
old-location: direct2d\ID2D1HwndRenderTarget.htm
tech.root: direct2d
ms.assetid: 860342cc-989c-4432-b879-07f3da07d50a
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ID2D1HwndRenderTarget, ID2D1HwndRenderTarget interface [Direct2D], ID2D1HwndRenderTarget interface [Direct2D],described, d2d1/ID2D1HwndRenderTarget, direct2d.ID2D1HwndRenderTarget
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - ID2D1HwndRenderTarget
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1HwndRenderTarget interface


## -description


Renders drawing instructions to a window.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID2D1HwndRenderTarget</b> interface inherits from <a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>. <b>ID2D1HwndRenderTarget</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID2D1HwndRenderTarget</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f40d46dc-04ec-4d11-bc3e-96043b16dcb3">CheckWindowState</a>
</td>
<td align="left" width="63%">
Indicates whether the HWND associated with this render target is occluded.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ba43ed30-fd29-4163-a2ea-15ba42e819db">GetHwnd</a>
</td>
<td align="left" width="63%">
Returns the HWND associated with this render target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b8ea2e96-c69b-4018-9572-c9099bf6202d">Resize</a>
</td>
<td align="left" width="63%">Overloaded. Changes the size of the render target to the specified pixel size.

</td>
</tr>
</table> 


## -remarks



As is the case with other render targets, you must call <a href="https://msdn.microsoft.com/0562b286-7427-4d76-b699-a39356496a0f">BeginDraw</a>  before issuing drawing commands. After you've finished drawing, call <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> to indicate that drawing is finished and to release access to the buffer backing the render target.

For <b>ID2D1HwndRenderTarget</b>, the only side effect of <b>BeginDraw</b> is changing the state of the render target to allow drawing commands to be issued.

<b>EndDraw</b> flushes any batched drawing commands. If no errors have occurred, then it also presents the buffer, causing it to appear on the associated window. Finally, <b>EndDraw</b> returns the HRESULT of the first error that occurred in drawing or presenting, as well as the tag state at the time the error occurred.

<b>ID2D1HwndRenderTarget</b> objects are double buffered, so drawing commands issued do not appear immediately, but rather are performed on an offscreen surface. When <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> is called, if there have been no rendering errors, the offscreen buffer is presented. If there have been rendering errors in the batch flushed by <b>EndDraw</b>, then the buffer is not presented, and the application must call <a href="https://msdn.microsoft.com/0562b286-7427-4d76-b699-a39356496a0f">BeginDraw</a> and re-draw the frame. <a href="https://msdn.microsoft.com/3ad9c966-85f5-4ddb-a8c1-aefcba533509">Flush</a> can be used to check for errors before calling <b>EndDraw</b> if an application wants the frame to be presented regardless of errors.



A hardware render target's back-buffer is the size specified by <a href="https://msdn.microsoft.com/d0d736b5-0427-4c0d-8085-8498fd00f6b6">GetPixelSize</a>. If <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> presents the buffer, this bitmap is stretched to cover the surface where it is presented: the entire client area of the window. This stretch is performed using bilinear filtering if the render target is rendering in hardware and using nearest-neighbor filtering if the rendering target is using software. (Typically, an application will call <a href="https://msdn.microsoft.com/b8ea2e96-c69b-4018-9572-c9099bf6202d">Resize</a> to ensure the pixel size of the render target and the pixel size of the destination match, and no scaling is necessary, though this is not a requirement.)



In the case where a window straddles adapters, Direct2D ensures that the portion of the off-screen render target is copied from the adapter where rendering is occurring to the adapter that needs to display the contents.



If the adapter a render target is on has been removed or the driver upgraded while the application is running, this is returned as an error in the <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> call. In this case, the application should create a new render target and resources as necessary.


<h3><a id="Creating_ID2D1HwndRenderTarget_Objects"></a><a id="creating_id2d1hwndrendertarget_objects"></a><a id="CREATING_ID2D1HWNDRENDERTARGET_OBJECTS"></a>Creating ID2D1HwndRenderTarget Objects</h3>
To create an <b>ID2D1HwndRenderTarget</b>, use the <a href="https://msdn.microsoft.com/3b55b1b0-a423-40dc-9581-c1fbe8134ca5">ID2D1Factory::CreateHwndRenderTarget</a> method.

Your application should create render targets once and hold onto them for the life of the application or until the render target's  <a href="https://msdn.microsoft.com/a8f24501-4e85-4981-bb38-2bd6333a7b49">EndDraw</a> method returns the <a href="https://msdn.microsoft.com/018bfca5-6ef4-497c-a4b6-8502c3cdac1b">D2DERR_RECREATE_TARGET</a>  error. When you receive this error, you need to recreate the render target (and any resources it created).


#### Examples

The following example uses the <a href="https://msdn.microsoft.com/3b55b1b0-a423-40dc-9581-c1fbe8134ca5">CreateHwndRenderTarget</a> method to create an <b>ID2D1HwndRenderTarget</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>RECT rc;
GetClientRect(m_hwnd, &amp;rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory-&gt;CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &amp;m_pRenderTarget
    );
</pre>
</td>
</tr>
</table></span></div>
The next example uses the <b>ID2D1HwndRenderTarget</b> to draw text to the window.

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
Code has been omitted from this example.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/40629be9-5840-4bde-b369-56bbfd791775">ID2D1RenderTarget</a>
 

 

