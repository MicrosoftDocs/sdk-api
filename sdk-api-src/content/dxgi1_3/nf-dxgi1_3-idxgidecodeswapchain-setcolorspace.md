---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.SetColorSpace
title: IDXGIDecodeSwapChain::SetColorSpace (dxgi1_3.h)
description: Sets the color space used by the swap chain. (IDXGIDecodeSwapChain.SetColorSpace)
helpviewer_keywords: ["IDXGIDecodeSwapChain interface [DXGI]","SetColorSpace method","IDXGIDecodeSwapChain.SetColorSpace","IDXGIDecodeSwapChain::SetColorSpace","SetColorSpace","SetColorSpace method [DXGI]","SetColorSpace method [DXGI]","IDXGIDecodeSwapChain interface","direct3ddxgi.idxgidecodeswapchain_setcolorspace","dxgi1_3/IDXGIDecodeSwapChain::SetColorSpace"]
old-location: direct3ddxgi\idxgidecodeswapchain_setcolorspace.htm
tech.root: direct3ddxgi
ms.assetid: DE0AA2BF-8E98-4CF4-8CC2-760AB4B8776D
ms.date: 12/05/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],SetColorSpace method, IDXGIDecodeSwapChain.SetColorSpace, IDXGIDecodeSwapChain::SetColorSpace, SetColorSpace, SetColorSpace method [DXGI], SetColorSpace method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_setcolorspace, dxgi1_3/IDXGIDecodeSwapChain::SetColorSpace
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
 - IDXGIDecodeSwapChain::SetColorSpace
 - dxgi1_3/IDXGIDecodeSwapChain::SetColorSpace
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
 - IDXGIDecodeSwapChain.SetColorSpace
---

# IDXGIDecodeSwapChain::SetColorSpace


## -description

Sets the color space used by the swap chain.

## -parameters

### -param ColorSpace

A pointer to a combination of <a href="/windows/desktop/api/dxgi1_3/ne-dxgi1_3-dxgi_multiplane_overlay_ycbcr_flags">DXGI_MULTIPLANE_OVERLAY_YCbCr_FLAGS</a>-typed values that are combined by using a bitwise OR operation. The resulting value specifies the color space to set for the swap chain.

## -returns

This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>
