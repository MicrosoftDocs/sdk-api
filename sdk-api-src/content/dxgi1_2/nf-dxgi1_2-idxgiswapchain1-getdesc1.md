---
UID: NF:dxgi1_2.IDXGISwapChain1.GetDesc1
title: IDXGISwapChain1::GetDesc1 (dxgi1_2.h)
description: Gets a description of the swap chain.
helpviewer_keywords: ["GetDesc1","GetDesc1 method [DXGI]","GetDesc1 method [DXGI]","IDXGISwapChain1 interface","IDXGISwapChain1 interface [DXGI]","GetDesc1 method","IDXGISwapChain1.GetDesc1","IDXGISwapChain1::GetDesc1","direct3ddxgi.idxgiswapchain1_getdesc1","dxgi1_2/IDXGISwapChain1::GetDesc1"]
old-location: direct3ddxgi\idxgiswapchain1_getdesc1.htm
tech.root: direct3ddxgi
ms.assetid: 86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2
ms.date: 12/05/2018
ms.keywords: GetDesc1, GetDesc1 method [DXGI], GetDesc1 method [DXGI],IDXGISwapChain1 interface, IDXGISwapChain1 interface [DXGI],GetDesc1 method, IDXGISwapChain1.GetDesc1, IDXGISwapChain1::GetDesc1, direct3ddxgi.idxgiswapchain1_getdesc1, dxgi1_2/IDXGISwapChain1::GetDesc1
req.header: dxgi1_2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - IDXGISwapChain1::GetDesc1
 - dxgi1_2/IDXGISwapChain1::GetDesc1
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
 - IDXGISwapChain1.GetDesc1
---

# IDXGISwapChain1::GetDesc1


## -description

Gets a description of the swap chain.

## -parameters

### -param pDesc [out]

A pointer to a <a href="/windows/desktop/api/dxgi1_2/ns-dxgi1_2-dxgi_swap_chain_desc1">DXGI_SWAP_CHAIN_DESC1</a>  structure that describes the swap chain.

## -returns

Returns S_OK if successful; an error code otherwise.  For a list of error codes, see <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a>.

## -see-also

<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>