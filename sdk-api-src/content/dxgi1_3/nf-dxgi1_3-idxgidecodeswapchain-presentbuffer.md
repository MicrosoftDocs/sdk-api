---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.PresentBuffer
title: IDXGIDecodeSwapChain::PresentBuffer (dxgi1_3.h)
description: Presents a frame on the output adapter.
helpviewer_keywords: ["IDXGIDecodeSwapChain interface [DXGI]","PresentBuffer method","IDXGIDecodeSwapChain.PresentBuffer","IDXGIDecodeSwapChain::PresentBuffer","PresentBuffer","PresentBuffer method [DXGI]","PresentBuffer method [DXGI]","IDXGIDecodeSwapChain interface","direct3ddxgi.idxgidecodeswapchain_presentbuffer","dxgi1_3/IDXGIDecodeSwapChain::PresentBuffer"]
old-location: direct3ddxgi\idxgidecodeswapchain_presentbuffer.htm
tech.root: direct3ddxgi
ms.assetid: EFBBE24E-9BA5-40CB-B090-EE0ADA1AF07D
ms.date: 12/05/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],PresentBuffer method, IDXGIDecodeSwapChain.PresentBuffer, IDXGIDecodeSwapChain::PresentBuffer, PresentBuffer, PresentBuffer method [DXGI], PresentBuffer method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_presentbuffer, dxgi1_3/IDXGIDecodeSwapChain::PresentBuffer
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGIDecodeSwapChain::PresentBuffer
 - dxgi1_3/IDXGIDecodeSwapChain::PresentBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIDecodeSwapChain.PresentBuffer
---

# IDXGIDecodeSwapChain::PresentBuffer


## -description

Presents a frame on the output adapter. The frame is a subresource of the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiresource">IDXGIResource</a> object that was used to create the decode swap chain.

## -parameters

### -param BufferToPresent

An index indicating which member of the subresource array to present.

### -param SyncInterval

An integer that specifies how to synchronize presentation of a frame with the vertical blank.


For the bit-block transfer (bitblt) model (<a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_DISCARD</a> or <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_SEQUENTIAL</a>), values are:

<ul>
<li>0 - The presentation occurs immediately, there is no synchronization.</li>
<li>1,2,3,4 - Synchronize presentation after the <i>n</i>th vertical blank.</li>
</ul>
For the flip model (<a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>), values are:

<ul>
<li>0 - Cancel the remaining time on the previously presented frame and discard this frame if a newer frame is queued.
</li>
<li>n &gt; 0 - Synchronize presentation for at least <i>n</i> vertical blanks.</li>
</ul>

### -param Flags

An integer value that contains swap-chain presentation options. These options are defined by the <a href="/windows/desktop/direct3ddxgi/dxgi-present">DXGI_PRESENT</a> constants.

The <b>DXGI_PRESENT_USE_DURATION</b> flag must be set if a custom present duration (custom refresh rate) is being used.

## -returns

This method returns <b>S_OK</b> on success, or it returns one of the following error codes:

<ul>
<li><a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_DEVICE_REMOVED</a></li>
<li><a href="/windows/desktop/direct3ddxgi/dxgi-status">DXGI_STATUS_OCCLUDED</a></li>
<li><a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR_INVALID_CALL</a></li>
<li><b>E_OUTOFMEMORY</b></li>
</ul>

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>