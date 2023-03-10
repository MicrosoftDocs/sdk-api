---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetColorSpace
title: IDXGIDecodeSwapChain::GetColorSpace (dxgi1_3.h)
description: Gets the color space used by the swap chain.
helpviewer_keywords: ["GetColorSpace","GetColorSpace method [DXGI]","GetColorSpace method [DXGI]","IDXGIDecodeSwapChain interface","IDXGIDecodeSwapChain interface [DXGI]","GetColorSpace method","IDXGIDecodeSwapChain.GetColorSpace","IDXGIDecodeSwapChain::GetColorSpace","direct3ddxgi.idxgidecodeswapchain_getcolorspace","dxgi1_3/IDXGIDecodeSwapChain::GetColorSpace"]
old-location: direct3ddxgi\idxgidecodeswapchain_getcolorspace.htm
tech.root: direct3ddxgi
ms.assetid: 3C63C75C-6395-46E8-9070-A62220FCA3B8
ms.date: 12/05/2018
ms.keywords: GetColorSpace, GetColorSpace method [DXGI], GetColorSpace method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetColorSpace method, IDXGIDecodeSwapChain.GetColorSpace, IDXGIDecodeSwapChain::GetColorSpace, direct3ddxgi.idxgidecodeswapchain_getcolorspace, dxgi1_3/IDXGIDecodeSwapChain::GetColorSpace
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
 - IDXGIDecodeSwapChain::GetColorSpace
 - dxgi1_3/IDXGIDecodeSwapChain::GetColorSpace
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
 - IDXGIDecodeSwapChain.GetColorSpace
---

# IDXGIDecodeSwapChain::GetColorSpace


## -description

Gets the color space used by the swap chain.



## -returns

A combination of <a href="/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags">DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies the color space for the swap chain.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>
