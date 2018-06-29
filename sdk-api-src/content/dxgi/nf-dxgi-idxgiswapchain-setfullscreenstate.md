---
UID: NF:dxgi.IDXGISwapChain.SetFullscreenState
title: IDXGISwapChain::SetFullscreenState
author: windows-sdk-content
description: Sets the display state to windowed or full screen.
old-location: direct3ddxgi\idxgiswapchain_setfullscreenstate.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_setfullscreenstate.htm
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: IDXGISwapChain interface [DXGI],SetFullscreenState method, IDXGISwapChain.SetFullscreenState, IDXGISwapChain::SetFullscreenState, SetFullscreenState, SetFullscreenState method [DXGI], SetFullscreenState method [DXGI],IDXGISwapChain interface, direct3ddxgi.idxgiswapchain_setfullscreenstate, dxgi/IDXGISwapChain::SetFullscreenState, f276366b-1618-a552-fa8f-29c081ebbe6d
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISwapChain.SetFullscreenState
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain::SetFullscreenState


## -description


Sets the display state to windowed or full screen.


## -parameters




### -param Fullscreen

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

A Boolean value that specifies whether to set the display state to windowed or full screen. <b>TRUE</b> for full screen, and <b>FALSE</b> for windowed.


### -param pTarget [in, optional]

Type: <b><a href="https://msdn.microsoft.com/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a>*</b>

If you pass <b>TRUE</b> to the <i>Fullscreen</i> parameter to set the display state to full screen, you can optionally set this parameter to a pointer to an <a href="https://msdn.microsoft.com/library/Bb174546(v=VS.85).aspx">IDXGIOutput</a> interface for the output target that contains the swap chain. If you set this parameter to <b>NULL</b>, DXGI will choose the output based on the swap-chain's device and the output window's 
        placement. If you pass <b>FALSE</b> to <i>Fullscreen</i>, you must set this parameter to <b>NULL</b>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This methods returns:
        

<ul>
<li>S_OK if the action succeeded and the swap chain was placed in the requested state.</li>
<li>DXGI_ERROR_NOT_CURRENTLY_AVAILABLE if the action failed. There are many reasons why a windowed-mode swap chain cannot switch to full-screen mode. For instance:

	          <ul>
<li>The application is running over Terminal Server.</li>
<li>The output window is occluded.</li>
<li>The output window does not have keyboard focus.</li>
<li>Another application is already in full-screen mode.</li>
</ul>
When this error is returned, an application can continue to run in windowed mode and try to switch to full-screen mode later.

</li>
<li>DXGI_STATUS_MODE_CHANGE_IN_PROGRESS is returned if a fullscreen/windowed mode transition is occurring when this API is called.</li>
<li>Other error codes if you run out of memory or encounter another unexpected fault; these codes may be treated as hard, non-continuable errors.</li>
</ul>



## -remarks



DXGI may change the display state of a swap chain in response to end user or system requests.

We recommend that you create a windowed swap chain and allow the end user to change the swap chain to full screen through <b>SetFullscreenState</b>; that is, do not set the <b>Windowed</b> member of <a href="https://msdn.microsoft.com/library/Bb173075(v=VS.85).aspx">DXGI_SWAP_CHAIN_DESC</a> to FALSE to force the swap chain to be full screen. However, if you create the swap chain as full screen, also provide the end user with a list of supported display modes because a swap chain that is created with an unsupported display mode might cause the display to go black and prevent the end user from seeing anything. Also, we recommend that you have a time-out confirmation screen or other fallback mechanism when you allow the end user to change display modes.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app calls <b>SetFullscreenState</b> to set the display state to full screen, <b>SetFullscreenState</b> fails with <a href="https://msdn.microsoft.com/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

You cannot call <b>SetFullscreenState</b> on a swap chain that you created with <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>.

For the <a href="https://msdn.microsoft.com/E132DAF5-80B7-4C52-A760-3779CC140CE7">flip presentation model</a>, after you transition the display state to full screen, you must call <a href="https://msdn.microsoft.com/library/Bb174577(v=VS.85).aspx">ResizeBuffers</a> to ensure that your call to <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> succeeds.




## -see-also




<a href="https://msdn.microsoft.com/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

