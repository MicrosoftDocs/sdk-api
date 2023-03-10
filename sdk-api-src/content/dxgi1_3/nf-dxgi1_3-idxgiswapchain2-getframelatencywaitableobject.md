---
UID: NF:dxgi1_3.IDXGISwapChain2.GetFrameLatencyWaitableObject
title: IDXGISwapChain2::GetFrameLatencyWaitableObject (dxgi1_3.h)
description: Returns a waitable handle that signals when the DXGI adapter has finished presenting a new frame.
helpviewer_keywords: ["GetFrameLatencyWaitableObject","GetFrameLatencyWaitableObject method [DXGI]","GetFrameLatencyWaitableObject method [DXGI]","IDXGISwapChain2 interface","IDXGISwapChain2 interface [DXGI]","GetFrameLatencyWaitableObject method","IDXGISwapChain2.GetFrameLatencyWaitableObject","IDXGISwapChain2::GetFrameLatencyWaitableObject","direct3ddxgi.idxgiswapchain2_getframelatencywaitableobject","dxgi1_3/IDXGISwapChain2::GetFrameLatencyWaitableObject"]
old-location: direct3ddxgi\idxgiswapchain2_getframelatencywaitableobject.htm
tech.root: direct3ddxgi
ms.assetid: 70E7347F-C6F9-49FA-9796-B728CF3F7778
ms.date: 12/05/2018
ms.keywords: GetFrameLatencyWaitableObject, GetFrameLatencyWaitableObject method [DXGI], GetFrameLatencyWaitableObject method [DXGI],IDXGISwapChain2 interface, IDXGISwapChain2 interface [DXGI],GetFrameLatencyWaitableObject method, IDXGISwapChain2.GetFrameLatencyWaitableObject, IDXGISwapChain2::GetFrameLatencyWaitableObject, direct3ddxgi.idxgiswapchain2_getframelatencywaitableobject, dxgi1_3/IDXGISwapChain2::GetFrameLatencyWaitableObject
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
 - IDXGISwapChain2::GetFrameLatencyWaitableObject
 - dxgi1_3/IDXGISwapChain2::GetFrameLatencyWaitableObject
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
 - IDXGISwapChain2.GetFrameLatencyWaitableObject
---

# IDXGISwapChain2::GetFrameLatencyWaitableObject


## -description

Returns a waitable handle that signals when the DXGI adapter has finished presenting a new frame.

Windows 8.1 introduces new APIs that allow lower-latency rendering by waiting  until the previous frame is presented to the display before drawing the next frame. To use this method, first create the DXGI swap chain with the <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT</a> flag set, then call <b>GetFrameLatencyWaitableObject</b> to retrieve the waitable handle. Use the waitable handle with <a href="/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobjectex">WaitForSingleObjectEx</a> to synchronize rendering of each new frame with the end of the previous frame. For every frame it renders, the app should wait on this handle before starting any rendering operations. Note that this requirement includes the first frame the app renders with the swap chain. See the <a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20latency%20sample">DirectXLatency sample</a>. When you are done with the handle, use <a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> to close it.



## -returns

A handle to the waitable object, or NULL if the swap chain was not created with <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_chain_flag">DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT</a>.

## -remarks

When an application is finished using the object handle returned by
**IDXGISwapChain2::GetFrameLatencyWaitableObject**, use the <a href="/windows/win32/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function to close the handle.

## -see-also

<a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/master/Official%20Windows%20Platform%20Sample/DirectX%20latency%20sample">DirectX latency sample</a>

<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency">GetMaximumFrameLatency</a>

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>

<a href="/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency">SetMaximumFrameLatency</a>
