---
UID: NF:dxgi.IDXGISwapChain.GetBuffer
title: IDXGISwapChain::GetBuffer (dxgi.h)
description: Accesses one of the swap-chain's back buffers.
helpviewer_keywords: ["GetBuffer","GetBuffer method [DXGI]","GetBuffer method [DXGI]","IDXGISwapChain interface","IDXGISwapChain interface [DXGI]","GetBuffer method","IDXGISwapChain.GetBuffer","IDXGISwapChain::GetBuffer","bd427578-fb6a-3136-aa3f-221b9262700c","direct3ddxgi.idxgiswapchain_getbuffer","dxgi/IDXGISwapChain::GetBuffer"]
old-location: direct3ddxgi\idxgiswapchain_getbuffer.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getbuffer.htm
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [DXGI], GetBuffer method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetBuffer method, IDXGISwapChain.GetBuffer, IDXGISwapChain::GetBuffer, bd427578-fb6a-3136-aa3f-221b9262700c, direct3ddxgi.idxgiswapchain_getbuffer, dxgi/IDXGISwapChain::GetBuffer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDXGISwapChain::GetBuffer
 - dxgi/IDXGISwapChain::GetBuffer
dev_langs:
 - c++
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
---

# IDXGISwapChain::GetBuffer


## -description

Accesses one of the swap-chain's back buffers.

## -parameters

### -param Buffer

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based buffer index. 

If the swap chain's swap effect is <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_DISCARD</a>, this method can only access the first buffer; for this situation, set the index to zero.

If the swap chain's swap effect is either <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_SEQUENTIAL</a>, only the swap chain's zero-index buffer can be read from and written to. The swap chain's buffers with indexes greater than zero can only be read from; so if you call the <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgiresource-getusage">IDXGIResource::GetUsage</a> method for such buffers, they have the <a href="/windows/desktop/direct3ddxgi/dxgi-usage">DXGI_USAGE_READ_ONLY</a> flag set.

If the swap chain's swap effect is <a href="/windows/desktop/api/dxgi/ne-dxgi-dxgi_swap_effect">DXGI_SWAP_EFFECT_FLIP_SEQUENTIAL</a>, the relationship between indices and buffers is consistent. The result is identical if you get the swap chain's zero-index buffer after each time <a href="windows/win32/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> is called. A correct frame index should be used to retrieve the current backbuffer.

### -param riid [in]

Type: <b>REFIID</b>

The type of interface used to manipulate the buffer.

### -param ppSurface [out]

Type: <b>void**</b>

A pointer to a back-buffer interface.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>