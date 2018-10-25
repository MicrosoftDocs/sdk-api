---
UID: NF:dxgi.IDXGISwapChain.GetBuffer
title: IDXGISwapChain::GetBuffer
author: windows-sdk-content
description: Accesses one of the swap-chain's back buffers.
old-location: direct3ddxgi\idxgiswapchain_getbuffer.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getbuffer.htm
ms.author: windowssdkdev
ms.date: 10/24/2018
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

If the swap chain's swap effect is <a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_DISCARD</a>, this method can only access the first buffer; for this situation, set the index to zero.

If the swap chain's swap effect is either <a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_SEQUENTIAL</a> or <a href="DXGI_SWAP_EFFECT.htm">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>, only the swap chain's zero-index buffer can be read from and written to. The swap chain's buffers with indexes greater than zero can only be read from; so if you call the <a href="https://msdn.microsoft.com/d5e44fba-14d9-4c30-b9b8-e3143aabcee4">IDXGIResource::GetUsage</a> method for such buffers, they have the <a href="dxgi_usage.htm">DXGI_USAGE_READ_ONLY</a> flag set.


### -param riid [in]

Type: <b>REFIID</b>

The type of interface used to manipulate the buffer.


### -param ppSurface [out]

Type: <b>void**</b>

A pointer to a back-buffer interface.


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

Returns one of the following <a href="https://msdn.microsoft.com/9aa7dd65-6bf9-4731-8085-a9eab4224cdd">DXGI_ERROR</a>.




## -see-also




<a href="https://msdn.microsoft.com/344ada45-35a0-4e99-b3b7-0f316df029ab">IDXGISwapChain</a>
 

 

