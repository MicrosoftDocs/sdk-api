---
UID: NF:dxgi1_3.IDXGISwapChain2.GetMaximumFrameLatency
title: IDXGISwapChain2::GetMaximumFrameLatency (dxgi1_3.h)
description: Gets the number of frames that the swap chain is allowed to queue for rendering.
helpviewer_keywords: ["GetMaximumFrameLatency","GetMaximumFrameLatency method [DXGI]","GetMaximumFrameLatency method [DXGI]","IDXGISwapChain2 interface","IDXGISwapChain2 interface [DXGI]","GetMaximumFrameLatency method","IDXGISwapChain2.GetMaximumFrameLatency","IDXGISwapChain2::GetMaximumFrameLatency","direct3ddxgi.idxgiswapchain2_getmaximumframelatency","dxgi1_3/IDXGISwapChain2::GetMaximumFrameLatency"]
old-location: direct3ddxgi\idxgiswapchain2_getmaximumframelatency.htm
tech.root: direct3ddxgi
ms.assetid: F0A07900-8F10-475B-B13F-E0F49B50C2EB
ms.date: 12/05/2018
ms.keywords: GetMaximumFrameLatency, GetMaximumFrameLatency method [DXGI], GetMaximumFrameLatency method [DXGI],IDXGISwapChain2 interface, IDXGISwapChain2 interface [DXGI],GetMaximumFrameLatency method, IDXGISwapChain2.GetMaximumFrameLatency, IDXGISwapChain2::GetMaximumFrameLatency, direct3ddxgi.idxgiswapchain2_getmaximumframelatency, dxgi1_3/IDXGISwapChain2::GetMaximumFrameLatency
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
 - IDXGISwapChain2::GetMaximumFrameLatency
 - dxgi1_3/IDXGISwapChain2::GetMaximumFrameLatency
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
 - IDXGISwapChain2.GetMaximumFrameLatency
---

# IDXGISwapChain2::GetMaximumFrameLatency


## -description

Gets the number of frames that the swap chain is allowed to queue for rendering.

## -parameters

### -param pMaxLatency [out]

The maximum number of back buffer frames that will be queued for the swap chain. This value is 1 by default, but should be set to 2 if the scene takes longer than it takes for one vertical refresh (typically about 16ms) to draw.

## -returns

Returns S_OK if successful; otherwise, returns one of the following members of the <a href="/windows/desktop/direct3d9/d3derr">D3DERR</a> enumerated type:

<ul>
<li><b>D3DERR_DEVICELOST</b></li>
<li><b>D3DERR_DEVICEREMOVED</b></li>
<li><b>D3DERR_DRIVERINTERNALERROR</b></li>
<li><b>D3DERR_INVALIDCALL</b></li>
<li><b>D3DERR_OUTOFVIDEOMEMORY</b></li>
</ul>

## -see-also

<a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20latency%20sample">DirectX latency sample</a>

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>

<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency">SetMaximumFrameLatency</a>