---
UID: NF:dxgi.IDXGISwapChain.ResizeTarget
title: IDXGISwapChain::ResizeTarget (dxgi.h)
description: Resizes the output target.
helpviewer_keywords: ["IDXGISwapChain interface [DXGI]","ResizeTarget method","IDXGISwapChain.ResizeTarget","IDXGISwapChain::ResizeTarget","ResizeTarget","ResizeTarget method [DXGI]","ResizeTarget method [DXGI]","IDXGISwapChain interface","direct3ddxgi.idxgiswapchain_resizetarget","dxgi/IDXGISwapChain::ResizeTarget","f136baf7-17fc-2a80-f25e-e0fc612bcad7"]
old-location: direct3ddxgi\idxgiswapchain_resizetarget.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_resizetarget.htm
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain interface [DXGI],ResizeTarget method, IDXGISwapChain.ResizeTarget, IDXGISwapChain::ResizeTarget, ResizeTarget, ResizeTarget method [DXGI], ResizeTarget method [DXGI],IDXGISwapChain interface, direct3ddxgi.idxgiswapchain_resizetarget, dxgi/IDXGISwapChain::ResizeTarget, f136baf7-17fc-2a80-f25e-e0fc612bcad7
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
 - IDXGISwapChain::ResizeTarget
 - dxgi/IDXGISwapChain::ResizeTarget
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
 - IDXGISwapChain.ResizeTarget
---

# IDXGISwapChain::ResizeTarget


## -description

Resizes the output target.

## -parameters

### -param pNewTargetParameters [in]

Type: <b>const <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a>*</b>

A pointer to a <a href="/previous-versions/windows/desktop/legacy/bb173064(v=vs.85)">DXGI_MODE_DESC</a> structure that describes the mode, which specifies the new width, height, format, and refresh rate of the target. 
        If the format is <a href="/windows/desktop/api/dxgiformat/ne-dxgiformat-dxgi_format">DXGI_FORMAT_UNKNOWN</a>, <b>ResizeTarget</b> uses the existing format. We only recommend that you use <b>DXGI_FORMAT_UNKNOWN</b> when the swap chain is in full-screen 
        mode as this method is not thread safe.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns a code that indicates success or failure. <b>DXGI_STATUS_MODE_CHANGE_IN_PROGRESS</b> is returned if a full-screen/windowed mode transition is occurring 
      when this API is called. See <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> for additional DXGI error codes.

## -remarks

<b>ResizeTarget</b> resizes the target window when the swap chain is in windowed mode, and changes the display mode on the target output when the swap 
      chain is in full-screen mode. Therefore, apps can call <b>ResizeTarget</b> to resize the target window (rather than a Microsoft Win32API such as <a href="/windows/desktop/api/winuser/nf-winuser-setwindowpos">SetWindowPos</a>) 
      without knowledge of the swap chain display mode.

If a Windows Store app calls <b>ResizeTarget</b>, it fails with <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.

You cannot call <b>ResizeTarget</b> on a swap chain that you created with <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>.

Apps must still call <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers">IDXGISwapChain::ResizeBuffers</a> after they call <b>ResizeTarget</b> because only <b>ResizeBuffers</b> can change the back buffers. But, if those apps have implemented window resize processing to call <b>ResizeBuffers</b>, they don't need to explicitly call <b>ResizeBuffers</b> after they call <b>ResizeTarget</b> because the window resize processing will achieve what the app requires.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>