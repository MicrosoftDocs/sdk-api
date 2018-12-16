---
UID: NF:d3d10sdklayers.ID3D10Debug.SetSwapChain
title: ID3D10Debug::SetSwapChain
author: windows-sdk-content
description: Set a swap chain that the runtime will use for automatically calling Present.
old-location: direct3d10\id3d10debug_setswapchain.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug_setswapchain.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ID3D10Debug interface [Direct3D 10],SetSwapChain method, ID3D10Debug.SetSwapChain, ID3D10Debug::SetSwapChain, SetSwapChain, SetSwapChain method [Direct3D 10], SetSwapChain method [Direct3D 10],ID3D10Debug interface, b58e521c-faea-98fb-6fb5-01fb1131f1a6, d3d10sdklayers/ID3D10Debug::SetSwapChain, direct3d10.id3d10debug_setswapchain
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10SDKLayers.h
api_name:
 - ID3D10Debug.SetSwapChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D10Debug::SetSwapChain


## -description


Set a swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">Present</a>.


## -parameters




### -param pSwapChain [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>*</b>

Swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">Present</a>; must have been created with the <a href="https://msdn.microsoft.com/en-us/library/Bb174537(v=VS.85).aspx">DXGI_SWAP_EFFECT_SEQUENTIAL</a> swap-effect flag.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb205278(v=VS.85).aspx">Direct3D 10 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The swap chain set by this method will only be used if D3D10_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is set in the <a href="https://msdn.microsoft.com/en-us/library/Bb173520(v=VS.85).aspx">feature mask</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb173516(v=VS.85).aspx">ID3D10Debug Interface</a>
 

 

