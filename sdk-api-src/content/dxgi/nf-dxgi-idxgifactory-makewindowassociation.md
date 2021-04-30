---
UID: NF:dxgi.IDXGIFactory.MakeWindowAssociation
title: IDXGIFactory::MakeWindowAssociation (dxgi.h)
description: Allows DXGI to monitor an application's message queue for the alt-enter key sequence (which causes the application to switch from windowed to full screen or vice versa).
helpviewer_keywords: ["IDXGIFactory interface [DXGI]","MakeWindowAssociation method","IDXGIFactory.MakeWindowAssociation","IDXGIFactory::MakeWindowAssociation","MakeWindowAssociation","MakeWindowAssociation method [DXGI]","MakeWindowAssociation method [DXGI]","IDXGIFactory interface","cae30f32-d52e-b4d6-69fc-2b5a2a52afef","direct3ddxgi.idxgifactory_makewindowassociation","dxgi/IDXGIFactory::MakeWindowAssociation"]
old-location: direct3ddxgi\idxgifactory_makewindowassociation.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_makewindowassociation.htm
ms.date: 12/05/2018
ms.keywords: IDXGIFactory interface [DXGI],MakeWindowAssociation method, IDXGIFactory.MakeWindowAssociation, IDXGIFactory::MakeWindowAssociation, MakeWindowAssociation, MakeWindowAssociation method [DXGI], MakeWindowAssociation method [DXGI],IDXGIFactory interface, cae30f32-d52e-b4d6-69fc-2b5a2a52afef, direct3ddxgi.idxgifactory_makewindowassociation, dxgi/IDXGIFactory::MakeWindowAssociation
req.header: dxgi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: DXGI.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIFactory::MakeWindowAssociation
 - dxgi/IDXGIFactory::MakeWindowAssociation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGIFactory.MakeWindowAssociation
---

## -description

Allows DXGI to monitor an application's message queue for the alt-enter key sequence (which causes the application to switch from windowed to full screen or vice versa).

## -parameters

### -param WindowHandle

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HWND</a></b>

The handle of the window that is to be monitored. This parameter can be <b>NULL</b>; but only if *Flags* is also 0.

### -param Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

One or more of the following values.

<ul>
<li>DXGI_MWA_NO_WINDOW_CHANGES - Prevent DXGI from monitoring an applications message queue; this makes DXGI unable to respond to mode changes.</li>
<li>DXGI_MWA_NO_ALT_ENTER - Prevent DXGI from responding to an alt-enter sequence.</li>
<li>DXGI_MWA_NO_PRINT_SCREEN - Prevent DXGI from responding to a print-screen key.</li>
</ul>

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

<a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a> if <i>WindowHandle</i> is invalid, or E_OUTOFMEMORY.

## -remarks

<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The combination of <i>WindowHandle</i> and <i>Flags</i> informs DXGI to stop monitoring window messages for the previously-associated window.

If the application switches to full-screen mode, DXGI will choose a full-screen resolution to be the smallest supported resolution that is larger or the same size as the current back buffer size.

Applications can make some changes to make the transition from windowed to full screen more efficient. For example, on a WM_SIZE message, the application should release any outstanding swap-chain back buffers, call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers">IDXGISwapChain::ResizeBuffers</a>, then re-acquire the back buffers from the swap chain(s). This gives the swap chain(s) an opportunity to resize the back buffers, and/or recreate them to enable full-screen flipping operation. If the application does not perform this sequence, DXGI will still make the full-screen/windowed transition, but may be forced to use a stretch operation (since the back buffers may not be the correct size), which may be less efficient. Even if a stretch is not required, presentation may not be optimal because the back buffers might not be directly interchangeable with the front buffer. Thus, a call to <b>ResizeBuffers</b> on WM_SIZE is always recommended, since WM_SIZE is always sent during a fullscreen transition.

While windowed, the application can, if it chooses, restrict the size of its window's client area to sizes to which it is comfortable rendering. A fully flexible application would make no such restriction, but UI elements or other design considerations can, of course, make this flexibility untenable. If the application further chooses to restrict its window's client area to just those that match supported full-screen resolutions, the application can field WM_SIZING, then check against <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgioutput-findclosestmatchingmode">IDXGIOutput::FindClosestMatchingMode</a>. If a matching mode is found, allow the resize. (The IDXGIOutput can be retrieved from <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">IDXGISwapChain::GetContainingOutput</a>. Absent subsequent changes to desktop topology, this will be the same output that will be chosen when alt-enter is fielded and fullscreen mode is begun for that swap chain.)

Applications that want to handle mode changes or Alt+Enter themselves should call <b>MakeWindowAssociation</b> with the DXGI_MWA_NO_WINDOW_CHANGES flag after swap chain creation. The <i>WindowHandle</i> argument, if non-<b>NULL</b>, specifies that the application message queues will not be handled by the DXGI runtime for all swap chains of a particular target <a href="/windows/desktop/WinProg/windows-data-types">HWND</a>.  Calling <b>MakeWindowAssociation</b> with the DXGI_MWA_NO_WINDOW_CHANGES flag after swapchain creation ensures that DXGI will not interfere with application's handling of window mode changes or Alt+Enter.

You must call the **MakeWindowAssociation** method on the factory object associated with the target HWND swap chain(s). You can guarantee that by calling the [IDXGIObject::GetParent](/windows/win32/api/dxgi/nf-dxgi-idxgiobject-getparent) method on the swap chain(s) to locate the factory. Here's a code example of doing that.

```cppwinrt
void MakeWindowAssociationWithLocatedFactory(
    winrt::com_ptr<IDXGISwapChain> const& swapChain,
    HWND hWnd,
    UINT flags)
{
    winrt::com_ptr<IDXGIFactory1> factory;
    factory.capture(swapChain, &IDXGISwapChain::GetParent);
    factory->MakeWindowAssociation(hWnd, flags);
}
```

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app calls <b>MakeWindowAssociation</b>, it fails with <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

A Microsoft Win32 application can use <b>MakeWindowAssociation</b> to control full-screen transitions through the Alt+Enter key combination and print screen behavior for full screen.  For Windows Store apps, because DXGI can't perform full-screen transitions, a Windows Store app has no way to control full-screen transitions.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI interfaces</a>

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgifactory">IDXGIFactory</a>