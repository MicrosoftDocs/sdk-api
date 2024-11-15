---
UID: NF:dxgi.IDXGISwapChain.GetFrameStatistics
title: IDXGISwapChain::GetFrameStatistics (dxgi.h)
description: Gets performance statistics about the last render frame.
helpviewer_keywords: ["GetFrameStatistics","GetFrameStatistics method [DXGI]","GetFrameStatistics method [DXGI]","IDXGISwapChain interface","IDXGISwapChain interface [DXGI]","GetFrameStatistics method","IDXGISwapChain.GetFrameStatistics","IDXGISwapChain::GetFrameStatistics","direct3ddxgi.idxgiswapchain_getframestatistics","dxgi/IDXGISwapChain::GetFrameStatistics","f3c97ad1-9125-a209-1985-7dfedb3a35e2"]
old-location: direct3ddxgi\idxgiswapchain_getframestatistics.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getframestatistics.htm
ms.date: 12/05/2018
ms.keywords: GetFrameStatistics, GetFrameStatistics method [DXGI], GetFrameStatistics method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetFrameStatistics method, IDXGISwapChain.GetFrameStatistics, IDXGISwapChain::GetFrameStatistics, direct3ddxgi.idxgiswapchain_getframestatistics, dxgi/IDXGISwapChain::GetFrameStatistics, f3c97ad1-9125-a209-1985-7dfedb3a35e2
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
 - IDXGISwapChain::GetFrameStatistics
 - dxgi/IDXGISwapChain::GetFrameStatistics
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
 - IDXGISwapChain.GetFrameStatistics
---

# IDXGISwapChain::GetFrameStatistics


## -description

Gets performance statistics about the last render frame.

## -parameters

### -param pStats [out]

Type: <b><a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_frame_statistics">DXGI_FRAME_STATISTICS</a>*</b>

A pointer to a <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_frame_statistics">DXGI_FRAME_STATISTICS</a> structure for the frame statistics.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> values.

## -remarks

You cannot use <b>GetFrameStatistics</b> for swap chains that both use the bit-block transfer (bitblt) presentation model and draw in windowed mode.

You can only use <b>GetFrameStatistics</b> for swap chains that either use the flip presentation model or draw in full-screen mode. You set the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a> value in the <b>SwapEffect</b> member of the <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a> structure to specify that the swap chain uses the flip presentation model.

Statistics are not reliable in many multiple monitor scenarios, as well as scenarios where other fullscreen apps are running.

It may be necessary to call <b>DwmFlush</b> before frame statistics are updated on systems that support Hardware Flip Queue.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>
