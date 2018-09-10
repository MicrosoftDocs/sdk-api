---
UID: NF:dxgi1_3.IDXGISwapChain2.GetMaximumFrameLatency
title: IDXGISwapChain2::GetMaximumFrameLatency
author: windows-sdk-content
description: Gets the number of frames that the swap chain is allowed to queue for rendering.
old-location: direct3ddxgi\idxgiswapchain2_getmaximumframelatency.htm
tech.root: direct3ddxgi
ms.assetid: F0A07900-8F10-475B-B13F-E0F49B50C2EB
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetMaximumFrameLatency, GetMaximumFrameLatency method [DXGI], GetMaximumFrameLatency method [DXGI],IDXGISwapChain2 interface, IDXGISwapChain2 interface [DXGI],GetMaximumFrameLatency method, IDXGISwapChain2.GetMaximumFrameLatency, IDXGISwapChain2::GetMaximumFrameLatency, direct3ddxgi.idxgiswapchain2_getmaximumframelatency, dxgi1_3/IDXGISwapChain2::GetMaximumFrameLatency
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
 - IDXGISwapChain2.GetMaximumFrameLatency
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain2::GetMaximumFrameLatency


## -description


Gets the number of frames that the swap chain is allowed to queue for rendering.


## -parameters




### -param pMaxLatency [out]

The maximum number of back buffer frames that will be queued for the swap chain. This value is 1 by default, but should be set to 2 if the scene takes longer than it takes for one vertical refresh (typically about 16ms) to draw.


## -returns



Returns S_OK if successful; otherwise, returns one of the following members of the <a href="https://msdn.microsoft.com/4a9daa05-74f3-4173-b63d-53767feea7e2">D3DERR</a> enumerated type:

<ul>
<li><b>D3DERR_DEVICELOST</b></li>
<li><b>D3DERR_DEVICEREMOVED</b></li>
<li><b>D3DERR_DRIVERINTERNALERROR</b></li>
<li><b>D3DERR_INVALIDCALL</b></li>
<li><b>D3DERR_OUTOFVIDEOMEMORY</b></li>
</ul>



## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=320129">DirectX latency sample</a>



<a href="https://msdn.microsoft.com/1E14EAF6-5EEA-4B4A-8F5F-0BC779093654">IDXGISwapChain2</a>



<a href="https://msdn.microsoft.com/AF3F03F2-38B4-474A-8A66-86A93D776EA0">SetMaximumFrameLatency</a>
 

 

