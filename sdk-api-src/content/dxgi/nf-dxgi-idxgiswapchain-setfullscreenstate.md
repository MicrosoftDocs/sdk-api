---
UID: NF:dxgi.IDXGISwapChain.SetFullscreenState
title: IDXGISwapChain::SetFullscreenState (dxgi.h)
description: Sets the display state to windowed or full screen.
helpviewer_keywords: ["IDXGISwapChain interface [DXGI]","SetFullscreenState method","IDXGISwapChain.SetFullscreenState","IDXGISwapChain::SetFullscreenState","SetFullscreenState","SetFullscreenState method [DXGI]","SetFullscreenState method [DXGI]","IDXGISwapChain interface","direct3ddxgi.idxgiswapchain_setfullscreenstate","dxgi/IDXGISwapChain::SetFullscreenState","f276366b-1618-a552-fa8f-29c081ebbe6d"]
old-location: direct3ddxgi\idxgiswapchain_setfullscreenstate.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_setfullscreenstate.htm
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain interface [DXGI],SetFullscreenState method, IDXGISwapChain.SetFullscreenState, IDXGISwapChain::SetFullscreenState, SetFullscreenState, SetFullscreenState method [DXGI], SetFullscreenState method [DXGI],IDXGISwapChain interface, direct3ddxgi.idxgiswapchain_setfullscreenstate, dxgi/IDXGISwapChain::SetFullscreenState, f276366b-1618-a552-fa8f-29c081ebbe6d
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
 - IDXGISwapChain::SetFullscreenState
 - dxgi/IDXGISwapChain::SetFullscreenState
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
 - IDXGISwapChain.SetFullscreenState
---

## -description

Sets the display state to windowed or full screen.

## -parameters

### -param Fullscreen

Type: <b><a href="/windows/win32/WinProg/windows-data-types">BOOL</a></b>

A Boolean value that specifies whether to set the display state to windowed or full screen. <b>TRUE</b> for full screen, and <b>FALSE</b> for windowed.

### -param pTarget

Type: [in, optional] <b><a href="/windows/win32/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a>*</b>

If you pass <b>TRUE</b> to the <i>Fullscreen</i> parameter to set the display state to full screen, you can optionally set this parameter to a pointer to an <a href="/windows/win32/api/dxgi/nn-dxgi-idxgioutput">IDXGIOutput</a> interface for the output target that contains the swap chain. If you set this parameter to <b>NULL</b>, DXGI will choose the output based on the swap-chain's device and the output window's placement. If you pass <b>FALSE</b> to <i>Fullscreen</i>, then you must set this parameter to <b>NULL</b>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of these values.

- **S_OK** if the action succeeded and the swap chain was placed in the requested state.
- **DXGI_ERROR_NOT_CURRENTLY_AVAILABLE** if the action failed. When this error is returned, your application can continue to run in windowed mode and try to switch to full-screen mode later. There are many reasons why a windowed-mode swap chain cannot switch to full-screen mode. Here are some examples.
  - The application is running over Terminal Server.
  - The output window is occluded.
  - The output window does not have keyboard focus.
  - Another application is already in full-screen mode.
- **DXGI_STATUS_MODE_CHANGE_IN_PROGRESS** is returned if a fullscreen/windowed mode transition is occurring when this API is called.
- Other error codes if you run out of memory or encounter another unexpected fault; these codes may be treated as hard, non-continuable errors.

## -remarks

DXGI may change the display state of a swap chain in response to end user or system requests.

We recommend that you create a windowed swap chain and allow the end user to change the swap chain to full screen through <b>SetFullscreenState</b>; that is, do not set the <b>Windowed</b> member of <a href="/windows/win32/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a> to FALSE to force the swap chain to be full screen. However, if you create the swap chain as full screen, also provide the end user with a list of supported display modes because a swap chain that is created with an unsupported display mode might cause the display to go black and prevent the end user from seeing anything. Also, we recommend that you have a time-out confirmation screen or other fallback mechanism when you allow the end user to change display modes.

<h3><a id="Notes_for_Windows_Store_apps"></a><a id="notes_for_windows_store_apps"></a><a id="NOTES_FOR_WINDOWS_STORE_APPS"></a>Notes for Windows Store apps</h3>
If a Windows Store app calls <b>SetFullscreenState</b> to set the display state to full screen, <b>SetFullscreenState</b> fails with <a href="/windows/win32/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

You cannot call <b>SetFullscreenState</b> on a swap chain that you created with <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>.

For the <a href="/windows/win32/direct3ddxgi/dxgi-flip-model">flip presentation model</a>, after you transition the display state to full screen, you must call <a href="/windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers">ResizeBuffers</a> to ensure that your call to <a href="/windows/win32/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> succeeds.

## -see-also

<a href="/windows/win32/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>

