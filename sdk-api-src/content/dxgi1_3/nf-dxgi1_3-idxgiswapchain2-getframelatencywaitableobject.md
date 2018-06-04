---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IDXGISwapChain2::GetFrameLatencyWaitableObject


## -description


Returns a waitable handle that signals when the DXGI adapter has finished presenting a new frame.

Windows 8.1 introduces new APIs that allow lower-latency rendering by waiting  until the previous frame is presented to the display before drawing the next frame. To use this method, first create the DXGI swap chain with the <a href="https://msdn.microsoft.com/c0030570-89ba-4586-a358-8c3b8c393a90">DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT</a> flag set, then call <b>GetFrameLatencyWaitableObject</b> to retrieve the waitable handle. Use the waitable handle with <a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a> to synchronize rendering of each new frame with the end of the previous frame. For every frame it renders, the app should wait on this handle before starting any rendering operations. Note that this requirement includes the first frame the app renders with the swap chain. See the <a href="http://go.microsoft.com/fwlink/p/?linkid=320129">DirectXLatency sample</a>.


## -parameters






## -returns



A handle to the waitable object, or NULL if the swap chain was not created with <a href="https://msdn.microsoft.com/c0030570-89ba-4586-a358-8c3b8c393a90">DXGI_SWAP_CHAIN_FLAG_FRAME_LATENCY_WAITABLE_OBJECT</a>.




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=320129">DirectX latency sample</a>



<a href="https://msdn.microsoft.com/F0A07900-8F10-475B-B13F-E0F49B50C2EB">GetMaximumFrameLatency</a>



<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>



<a href="https://msdn.microsoft.com/AF3F03F2-38B4-474A-8A66-86A93D776EA0">SetMaximumFrameLatency</a>
 

 

