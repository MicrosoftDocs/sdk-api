---
UID: NF:d3d10sdklayers.ID3D10Debug.SetSwapChain
title: ID3D10Debug::SetSwapChain method
author: windows-driver-content
description: Set a swap chain that the runtime will use for automatically calling Present.
old-location: direct3d10\id3d10debug_setswapchain.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setswapchain.htm
ms.author: windowsdriverdev
ms.date: 4/3/2018
ms.keywords: ID3D10Debug, ID3D10Debug interface [Direct3D 10], SetSwapChain method, ID3D10Debug::SetSwapChain, SetSwapChain method [Direct3D 10], SetSwapChain method [Direct3D 10], ID3D10Debug interface, SetSwapChain,ID3D10Debug.SetSwapChain, b58e521c-faea-98fb-6fb5-01fb1131f1a6, d3d10sdklayers/ID3D10Debug::SetSwapChain, direct3d10.id3d10debug_setswapchain
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
-	ID3D10Debug.SetSwapChain
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D10Debug::SetSwapChain method


## -description


Set a swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>.


## -parameters




### -param pSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>*</b>

Swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>; must have been created with the <a href="https://msdn.microsoft.com/c6c32336-fbea-420b-b0d9-1c1cf3893688">DXGI_SWAP_EFFECT_SEQUENTIAL</a> swap-effect flag.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/7b67d428-d000-4c3e-adc1-b5fc67a15a6a">Direct3D 10 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The swap chain set by this method will only be used if D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is set in the <a href="https://msdn.microsoft.com/e9404531-fdf4-48e0-9ab5-f4e5b32ae077">feature mask</a>.




## -see-also




<a href="https://msdn.microsoft.com/2971189b-5df2-4d0a-ad7b-28dbfd6d0af3">ID3D10Debug Interface</a>
 

 

