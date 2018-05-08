---
UID: NF:dxgi.IDXGIFactory.MakeWindowAssociation
title: IDXGIFactory::MakeWindowAssociation
author: windows-driver-content
description: Allows DXGI to monitor an application's message queue for the alt-enter key sequence (which causes the application to switch from windowed to full screen or vice versa).
old-location: direct3ddxgi\idxgifactory_makewindowassociation.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgifactory_makewindowassociation.htm
ms.author: windowsdriverdev
ms.date: 3/23/2018
ms.keywords: IDXGIFactory interface [DXGI],MakeWindowAssociation method, IDXGIFactory.MakeWindowAssociation, IDXGIFactory::MakeWindowAssociation, MakeWindowAssociation, MakeWindowAssociation method [DXGI], MakeWindowAssociation method [DXGI],IDXGIFactory interface, cae30f32-d52e-b4d6-69fc-2b5a2a52afef, direct3ddxgi.idxgifactory_makewindowassociation, dxgi/IDXGIFactory::MakeWindowAssociation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: DXGI_SWAP_EFFECT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	DXGI.lib
-	DXGI.dll
api_name:
-	IDXGIFactory.MakeWindowAssociation
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIFactory::MakeWindowAssociation


## -description


Allows DXGI to monitor an application's message queue for the alt-enter key sequence (which causes the application to switch from windowed to full screen or vice versa).


## -parameters




### -param WindowHandle

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window that is to be monitored. This parameter can be <b>NULL</b>; but only if the flags are also 0. 


### -param Flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

One or more of the following values:


<ul>
<li>DXGI_MWA_NO_WINDOW_CHANGES - Prevent DXGI from monitoring an applications message queue; this makes DXGI unable to respond to mode changes.</li>
<li>DXGI_MWA_NO_ALT_ENTER - Prevent DXGI from responding to an alt-enter sequence.</li>
<li>DXGI_MWA_NO_PRINT_SCREEN - Prevent DXGI from responding to a print-screen key.</li>
</ul>

## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>


<a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_INVALID_CALL</a> if <i>WindowHandle</i> is invalid, or E_OUTOFMEMORY.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="dxgi_error.htm">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The combination of <i>WindowHandle</i> and <i>Flags</i> informs DXGI to stop monitoring window messages for the previously-associated window.

If the application switches to full-screen mode, DXGI will choose a full-screen resolution to be the smallest supported resolution that is larger or the same size as the current back buffer size.

Applications can make some changes to make the transition from windowed to full screen more efficient. For example, on a WM_SIZE message, the application should release any outstanding swap-chain back buffers, call <a href="https://msdn.microsoft.com/c70aaad0-e742-4ff1-9d25-80d171f3f9de">IDXGISwapChain::ResizeBuffers</a>, then re-acquire the back buffers from the swap chain(s). This gives the swap chain(s) an opportunity to resize the back buffers, and/or recreate them to enable full-screen flipping operation. If the application does not perform this sequence, DXGI will still make the full-screen/windowed transition, but may be forced to use a stretch operation (since the back buffers may not be the correct size), which may be less efficient. Even if a stretch is not required, presentation may not be optimal because the back buffers might not be directly interchangeable with the front buffer. Thus, a call to <b>ResizeBuffers</b> on WM_SIZE is always recommended, since WM_SIZE is always sent during a fullscreen transition.

While windowed, the application can, if it chooses, restrict the size of its window's client area to sizes to which it is comfortable rendering. A fully flexible application would make no such restriction, but UI elements or other design considerations can, of course, make this flexibility untenable. If the application further chooses to restrict its window's client area to just those that match supported full-screen resolutions, the application can field WM_SIZING, then check against <a href="https://msdn.microsoft.com/f531ee0d-d934-4ab2-bb7a-2c29f521f4cb">IDXGIOutput::FindClosestMatchingMode</a>. If a matching mode is found, allow the resize. (The IDXGIOutput can be retrieved from <a href="https://msdn.microsoft.com/0ebc1ec3-87f3-46bc-8516-180d28740b38">IDXGISwapChain::GetContainingOutput</a>. Absent subsequent changes to desktop topology, this will be the same output that will be chosen when alt-enter is fielded and fullscreen mode is begun for that swap chain.)

Applications that want to handle mode changes or Alt+Enter themselves should call <b>MakeWindowAssociation</b> with the DXGI_MWA_NO_WINDOW_CHANGES flag after swap chain creation. The <i>WindowHandle</i> argument, if non-<b>NULL</b>, specifies that the application message queues will not be handled by the DXGI runtime for all swap chains of a particular target <a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a>.  Calling <b>MakeWindowAssociation</b> with the DXGI_MWA_NO_WINDOW_CHANGES flag after swapchain creation ensures that DXGI will not interfere with application's handling of window mode changes or Alt+Enter.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app calls <b>MakeWindowAssociation</b>, it fails with <a href="dxgi_error.htm">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

A Microsoft Win32 application can use <b>MakeWindowAssociation</b> to control full-screen transitions through the Alt+Enter key combination and print screen behavior for full screen.  For Windows Store apps, because DXGI can't perform full-screen transitions, a Windows Store app has no way to control full-screen transitions.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/642aac36-ca5a-4c62-b5cb-f9d35965ca2f">IDXGIFactory</a>
 

 

