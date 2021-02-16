---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.SetSourceRect
title: IDXGIDecodeSwapChain::SetSourceRect (dxgi1_3.h)
description: Sets the rectangle that defines the source region for the video processing blit operation.
helpviewer_keywords: ["IDXGIDecodeSwapChain interface [DXGI]","SetSourceRect method","IDXGIDecodeSwapChain.SetSourceRect","IDXGIDecodeSwapChain::SetSourceRect","SetSourceRect","SetSourceRect method [DXGI]","SetSourceRect method [DXGI]","IDXGIDecodeSwapChain interface","direct3ddxgi.idxgidecodeswapchain_setsourcerect","dxgi1_3/IDXGIDecodeSwapChain::SetSourceRect"]
old-location: direct3ddxgi\idxgidecodeswapchain_setsourcerect.htm
tech.root: direct3ddxgi
ms.assetid: E614D9C2-9AAC-4ADC-9B7B-99C47975DA07
ms.date: 12/05/2018
ms.keywords: IDXGIDecodeSwapChain interface [DXGI],SetSourceRect method, IDXGIDecodeSwapChain.SetSourceRect, IDXGIDecodeSwapChain::SetSourceRect, SetSourceRect, SetSourceRect method [DXGI], SetSourceRect method [DXGI],IDXGIDecodeSwapChain interface, direct3ddxgi.idxgidecodeswapchain_setsourcerect, dxgi1_3/IDXGIDecodeSwapChain::SetSourceRect
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
 - IDXGIDecodeSwapChain::SetSourceRect
 - dxgi1_3/IDXGIDecodeSwapChain::SetSourceRect
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
 - IDXGIDecodeSwapChain.SetSourceRect
---

# IDXGIDecodeSwapChain::SetSourceRect


## -description

Sets the rectangle that defines the source region for the video processing blit operation.

The source rectangle is the portion of the input surface that is blitted to the destination surface. The source rectangle is given in pixel coordinates, relative to the input surface.

## -parameters

### -param pRect

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure 
        that contains the source region to set for the swap chain.

## -returns

This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>