---
UID: NF:d3d11sdklayers.ID3D11Debug.SetSwapChain
title: ID3D11Debug::SetSwapChain
author: windows-sdk-content
description: Sets a swap chain that the runtime will use for automatically calling IDXGISwapChain::Present.
old-location: direct3d11\id3d11debug_setswapchain.htm
tech.root: direct3d11
ms.assetid: 554d56e7-8901-4b39-bc1e-6db6496263c8
ms.author: windowssdkdev
ms.date: 11/16/2018
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


Sets a swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a>.


## -parameters




### -param pSwapChain [in, optional]

Type: <b><a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>*</b>

Swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a>; must have been created with the DXGI_SWAP_EFFECT_SEQUENTIAL swap-effect flag.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

This method returns one of the following <a href="https://msdn.microsoft.com/c0856a58-b760-44e5-8acf-145720b403d1">Direct3D 11 Return Codes</a>.




## -remarks



<div class="alert"><b>Note</b>  If you call this API in a Session 0 process, it returns <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR_NOT_CURRENTLY_AVAILABLE</a>.</div>
<div> </div>
The swap chain set by this method will only be used if D3D11_DEBUG_FEATURE_PRESENT_PER_RENDER_OP is set in the <a href="https://msdn.microsoft.com/60f9da61-dc97-4b6d-b187-df3605ad9336">feature mask</a>.




## -see-also




<a href="https://msdn.microsoft.com/2c640295-7a91-4a7a-92d3-909d288eb0d6">ID3D11Debug Interface</a>
 

 

