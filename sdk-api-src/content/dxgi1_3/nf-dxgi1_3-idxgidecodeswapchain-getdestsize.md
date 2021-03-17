---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetDestSize
title: IDXGIDecodeSwapChain::GetDestSize (dxgi1_3.h)
description: Gets the size of the destination surface to use for the video processing blit operation.
helpviewer_keywords: ["GetDestSize","GetDestSize method [DXGI]","GetDestSize method [DXGI]","IDXGIDecodeSwapChain interface","IDXGIDecodeSwapChain interface [DXGI]","GetDestSize method","IDXGIDecodeSwapChain.GetDestSize","IDXGIDecodeSwapChain::GetDestSize","direct3ddxgi.idxgidecodeswapchain_getdestsize","dxgi1_3/IDXGIDecodeSwapChain::GetDestSize"]
old-location: direct3ddxgi\idxgidecodeswapchain_getdestsize.htm
tech.root: direct3ddxgi
ms.assetid: FA01A6C1-7731-4B30-845F-4C2514B6AD77
ms.date: 12/05/2018
ms.keywords: GetDestSize, GetDestSize method [DXGI], GetDestSize method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetDestSize method, IDXGIDecodeSwapChain.GetDestSize, IDXGIDecodeSwapChain::GetDestSize, direct3ddxgi.idxgidecodeswapchain_getdestsize, dxgi1_3/IDXGIDecodeSwapChain::GetDestSize
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
 - IDXGIDecodeSwapChain::GetDestSize
 - dxgi1_3/IDXGIDecodeSwapChain::GetDestSize
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
 - IDXGIDecodeSwapChain.GetDestSize
---

# IDXGIDecodeSwapChain::GetDestSize


## -description

Gets the size of the destination surface to use for the video processing blit operation.

## -parameters

### -param pWidth [out]

A pointer to a variable that receives the width in pixels.

### -param pHeight [out]

A pointer to a variable that receives the height in pixels.

## -returns

This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>