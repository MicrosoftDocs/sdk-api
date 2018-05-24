---
UID: NF:d3d10sdklayers.ID3D10Debug.GetSwapChain
title: ID3D10Debug::GetSwapChain
author: windows-driver-content
description: Get the swap chain that the runtime will use for automatically calling Present.
old-location: direct3d10\id3d10debug_getswapchain.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_getswapchain.htm
ms.author: windowsdriverdev
ms.date: 5/21/2018
ms.keywords: 0701d3b1-1d64-2987-0b96-e4018a8313df, GetSwapChain, GetSwapChain method [Direct3D 10], GetSwapChain method [Direct3D 10],ID3D10Debug interface, ID3D10Debug interface [Direct3D 10],GetSwapChain method, ID3D10Debug.GetSwapChain, ID3D10Debug::GetSwapChain, d3d10sdklayers/ID3D10Debug::GetSwapChain, direct3d10.id3d10debug_getswapchain
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d10sdklayers.h
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10SDKLayers.h
api_name:
-	ID3D10Debug.GetSwapChain
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Debug::GetSwapChain


## -description


Get the swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>.


## -parameters




### -param ppSwapChain [out]

Type: <b><a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>**</b>

Swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



The swap chain retrieved by this method will only be used if D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is set in the <a href="https://msdn.microsoft.com/e9404531-fdf4-48e0-9ab5-f4e5b32ae077">feature mask</a>.




## -see-also




<a href="https://msdn.microsoft.com/2971189b-5df2-4d0a-ad7b-28dbfd6d0af3">ID3D10Debug Interface</a>
 

 

