---
UID: NF:dxgi.IDXGISwapChain.GetDesc
title: IDXGISwapChain::GetDesc (dxgi.h)
description: Get a description of the swap chain.
helpviewer_keywords: ["545f3a98-5c81-337d-c4f7-cc715e0e123f","GetDesc","GetDesc method [DXGI]","GetDesc method [DXGI]","IDXGISwapChain interface","IDXGISwapChain interface [DXGI]","GetDesc method","IDXGISwapChain.GetDesc","IDXGISwapChain::GetDesc","direct3ddxgi.idxgiswapchain_getdesc","dxgi/IDXGISwapChain::GetDesc"]
old-location: direct3ddxgi\idxgiswapchain_getdesc.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain_getdesc.htm
ms.date: 12/05/2018
ms.keywords: 545f3a98-5c81-337d-c4f7-cc715e0e123f, GetDesc, GetDesc method [DXGI], GetDesc method [DXGI],IDXGISwapChain interface, IDXGISwapChain interface [DXGI],GetDesc method, IDXGISwapChain.GetDesc, IDXGISwapChain::GetDesc, direct3ddxgi.idxgiswapchain_getdesc, dxgi/IDXGISwapChain::GetDesc
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
 - IDXGISwapChain::GetDesc
 - dxgi/IDXGISwapChain::GetDesc
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
 - IDXGISwapChain.GetDesc
---

# IDXGISwapChain::GetDesc


## -description

<p class="CCE_Message">[Starting with Direct3D 11.1, we recommend not to use <b>GetDesc</b> anymore to get a description of the swap chain. Instead, use <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1">IDXGISwapChain1::GetDesc1</a>.]

Get a description of the swap chain.

## -parameters

### -param pDesc [out]

Type: <b><a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a>*</b>

A pointer to the swap-chain description (see <a href="/windows/desktop/api/dxgi/ns-dxgi-dxgi_swap_chain_desc">DXGI_SWAP_CHAIN_DESC</a>).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -see-also

<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>