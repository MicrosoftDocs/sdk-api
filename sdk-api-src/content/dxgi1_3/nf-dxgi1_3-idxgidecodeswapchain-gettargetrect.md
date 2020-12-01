---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetTargetRect
title: IDXGIDecodeSwapChain::GetTargetRect (dxgi1_3.h)
description: Gets the rectangle that defines the target region for the video processing blit operation.
helpviewer_keywords: ["GetTargetRect","GetTargetRect method [DXGI]","GetTargetRect method [DXGI]","IDXGIDecodeSwapChain interface","IDXGIDecodeSwapChain interface [DXGI]","GetTargetRect method","IDXGIDecodeSwapChain.GetTargetRect","IDXGIDecodeSwapChain::GetTargetRect","direct3ddxgi.idxgidecodeswapchain_gettargetrect","dxgi1_3/IDXGIDecodeSwapChain::GetTargetRect"]
old-location: direct3ddxgi\idxgidecodeswapchain_gettargetrect.htm
tech.root: direct3ddxgi
ms.assetid: 1B42CE33-7130-433F-940F-B45D3152BB33
ms.date: 12/05/2018
ms.keywords: GetTargetRect, GetTargetRect method [DXGI], GetTargetRect method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetTargetRect method, IDXGIDecodeSwapChain.GetTargetRect, IDXGIDecodeSwapChain::GetTargetRect, direct3ddxgi.idxgidecodeswapchain_gettargetrect, dxgi1_3/IDXGIDecodeSwapChain::GetTargetRect
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
 - IDXGIDecodeSwapChain::GetTargetRect
 - dxgi1_3/IDXGIDecodeSwapChain::GetTargetRect
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
 - IDXGIDecodeSwapChain.GetTargetRect
---

# IDXGIDecodeSwapChain::GetTargetRect


## -description

Gets the rectangle that defines the target region for the video processing blit operation.

## -parameters

### -param pRect [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure 
        that receives the target region for the swap chain.

## -returns

This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>