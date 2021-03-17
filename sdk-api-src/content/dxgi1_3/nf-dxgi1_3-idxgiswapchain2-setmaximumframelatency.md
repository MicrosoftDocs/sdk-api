---
UID: NF:dxgi1_3.IDXGISwapChain2.SetMaximumFrameLatency
title: IDXGISwapChain2::SetMaximumFrameLatency (dxgi1_3.h)
description: Sets the number of frames that the swap chain is allowed to queue for rendering.
helpviewer_keywords: ["IDXGISwapChain2 interface [DXGI]","SetMaximumFrameLatency method","IDXGISwapChain2.SetMaximumFrameLatency","IDXGISwapChain2::SetMaximumFrameLatency","SetMaximumFrameLatency","SetMaximumFrameLatency method [DXGI]","SetMaximumFrameLatency method [DXGI]","IDXGISwapChain2 interface","direct3ddxgi.idxgiswapchain2_setmaximumframelatency","dxgi1_3/IDXGISwapChain2::SetMaximumFrameLatency"]
old-location: direct3ddxgi\idxgiswapchain2_setmaximumframelatency.htm
tech.root: direct3ddxgi
ms.assetid: AF3F03F2-38B4-474A-8A66-86A93D776EA0
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain2 interface [DXGI],SetMaximumFrameLatency method, IDXGISwapChain2.SetMaximumFrameLatency, IDXGISwapChain2::SetMaximumFrameLatency, SetMaximumFrameLatency, SetMaximumFrameLatency method [DXGI], SetMaximumFrameLatency method [DXGI],IDXGISwapChain2 interface, direct3ddxgi.idxgiswapchain2_setmaximumframelatency, dxgi1_3/IDXGISwapChain2::SetMaximumFrameLatency
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dxgi.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain2::SetMaximumFrameLatency
 - dxgi1_3/IDXGISwapChain2::SetMaximumFrameLatency
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGISwapChain2.SetMaximumFrameLatency
---

# IDXGISwapChain2::SetMaximumFrameLatency


## -description

Sets the number of frames that the swap chain is allowed to queue for rendering.

## -parameters

### -param MaxLatency

The maximum number of back buffer frames that will be queued for the swap chain. This value is 1 by default.

## -returns

Returns S_OK if successful; otherwise, DXGI_ERROR_DEVICE_REMOVED if the device was removed.

## -remarks

This method is only valid for use on swap chains created with <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT</a>. Otherwise, the result will be DXGI_ERROR_INVALID_CALL.

## -see-also

<a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20latency%20sample">DirectX latency sample</a>

<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency">GetMaximumFrameLatency</a>

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>