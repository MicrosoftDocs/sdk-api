---
UID: NF:dxgi.IDXGISwapChain.GetBuffer
title: IDXGISwapChain::GetBuffer
author: windows-sdk-content
description: Accesses one of the swap-chain's back buffers.
old-location: direct3ddxgi\idxgiswapchain_getbuffer.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getbuffer.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetBuffer, GetBuffer method [DXGI], GetBuffer method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetBuffer method, IDXGISwapChain.GetBuffer, IDXGISwapChain::GetBuffer, bd427578-fb6a-3136-aa3f-221b9262700c, direct3ddxgi.idxgiswapchain_getbuffer, dxgi/IDXGISwapChain::GetBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: dxgi.h
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
req.lib: DXGI.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DXGI.lib
 - DXGI.dll
api_name:
 - IDXGISwapChain.GetBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain::GetBuffer


## -description


Accesses one of the swap-chain's back buffers.


## -parameters




### -param Buffer

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

A zero-based buffer index. 

If the swap chain's swap effect is <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_DISCARD</a>, this method can only access the first buffer; for this situation, set the index to zero.

If the swap chain's swap effect is either <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_SEQUENTIAL</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb173077(v=VS.85).aspx">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>, only the swap chain's zero-index buffer can be read from and written to. The swap chain's buffers with indexes greater than zero can only be read from; so if you call the <a href="https://msdn.microsoft.com/en-us/library/Bb174563(v=VS.85).aspx">IDXGIResource::GetUsage</a> method for such buffers, they have the <a href="https://msdn.microsoft.com/en-us/library/Bb173078(v=VS.85).aspx">DXGI_USAGE_READ_ONLY</a> flag set.


### -param riid [in]

Type: <b>REFIID</b>

The type of interface used to manipulate the buffer.


### -param ppSurface [out]

Type: <b>void**</b>

A pointer to a back-buffer interface.


## -returns



Type: <b><a href="https://msdn.microsoft.com/en-us/library/Hh437604(v=VS.85).aspx">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/en-us/library/Bb509553(v=VS.85).aspx">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb174569(v=VS.85).aspx">IDXGISwapChain</a>
 

 

