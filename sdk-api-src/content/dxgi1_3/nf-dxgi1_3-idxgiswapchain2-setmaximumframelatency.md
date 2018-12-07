---
UID: NF:dxgi1_3.IDXGISwapChain2.SetMaximumFrameLatency
title: IDXGISwapChain2::SetMaximumFrameLatency
author: windows-sdk-content
description: Sets the number of frames that the swap chain is allowed to queue for rendering.
old-location: direct3ddxgi\idxgiswapchain2_setmaximumframelatency.htm
tech.root: direct3ddxgi
ms.assetid: AF3F03F2-38B4-474A-8A66-86A93D776EA0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDXGISwapChain2 interface [DXGI],SetMaximumFrameLatency method, IDXGISwapChain2.SetMaximumFrameLatency, IDXGISwapChain2::SetMaximumFrameLatency, SetMaximumFrameLatency, SetMaximumFrameLatency method [DXGI], SetMaximumFrameLatency method [DXGI],IDXGISwapChain2 interface, direct3ddxgi.idxgiswapchain2_setmaximumframelatency, dxgi1_3/IDXGISwapChain2::SetMaximumFrameLatency
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain2::SetMaximumFrameLatency


## -description


Sets the number of frames that the swap chain is allowed to queue for rendering.


## -parameters




### -param MaxLatency

The maximum number of back buffer frames that will be queued for the swap chain. This value is 3 by default.


## -returns



Returns S_OK if successful; otherwise, DXGI_ERROR_DEVICE_REMOVED if the device was removed.




## -remarks



This method is only valid for use on swap chains created with <a href="https://msdn.microsoft.com/en-us/library/Bb173076(v=VS.85).aspx">DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT</a>. Otherwise, the result will be DXGI_ERROR_INVALID_CALL.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=320129">DirectX latency sample</a>



<a href="https://msdn.microsoft.com/F0A07900-8F10-475B-B13F-E0F49B50C2EB">GetMaximumFrameLatency</a>



<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>
 

 

