---
UID: NF:d3d11sdklayers.ID3D11Debug.SetSwapChain
title: ID3D11Debug::SetSwapChain
author: windows-sdk-content
description: Sets a swap chain that the runtime will use for automatically calling IDXGISwapChain::Present.
old-location: direct3d11\id3d11debug_setswapchain.htm
tech.root: direct3d11
ms.assetid: 554d56e7-8901-4b39-bc1e-6db6496263c8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: 93f55103-9ea2-645a-a17a-4dc52160d41b, ID3D11Debug interface [Direct3D 11],SetSwapChain method, ID3D11Debug.SetSwapChain, ID3D11Debug::SetSwapChain, SetSwapChain, SetSwapChain method [Direct3D 11], SetSwapChain method [Direct3D 11],ID3D11Debug interface, d3d11sdklayers/ID3D11Debug::SetSwapChain, direct3d11.id3d11debug_setswapchain
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d3d11sdklayers.h
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
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Debug.SetSwapChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Debug::SetSwapChain


## -description


Sets a swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a>.


## -parameters




### -param pSwapChain [in, optional]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>*</b>

Swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a>; must have been created with the DXGI_SWAP_EFFECT_SEQUENTIAL swap-effect flag.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Ff476174(v=VS.85).aspx">Direct3D 11 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The swap chain set by this method will only be used if D3D11_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is set in the <a href="https://msdn.microsoft.com/en-us/library/Ff476371(v=VS.85).aspx">feature mask</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476366(v=VS.85).aspx">ID3D11Debug Interface</a>
 

 

