---
UID: NF:dxgi1_3.IDXGIDecodeSwapChain.GetSourceRect
title: IDXGIDecodeSwapChain::GetSourceRect (dxgi1_3.h)
description: Gets the source region that is used for the swap chain.
helpviewer_keywords: ["GetSourceRect","GetSourceRect method [DXGI]","GetSourceRect method [DXGI]","IDXGIDecodeSwapChain interface","IDXGIDecodeSwapChain interface [DXGI]","GetSourceRect method","IDXGIDecodeSwapChain.GetSourceRect","IDXGIDecodeSwapChain::GetSourceRect","direct3ddxgi.idxgidecodeswapchain_getsourcerect","dxgi1_3/IDXGIDecodeSwapChain::GetSourceRect"]
old-location: direct3ddxgi\idxgidecodeswapchain_getsourcerect.htm
tech.root: direct3ddxgi
ms.assetid: 67DD1267-997A-4D84-BC91-D124ED1E8946
ms.date: 12/05/2018
ms.keywords: GetSourceRect, GetSourceRect method [DXGI], GetSourceRect method [DXGI],IDXGIDecodeSwapChain interface, IDXGIDecodeSwapChain interface [DXGI],GetSourceRect method, IDXGIDecodeSwapChain.GetSourceRect, IDXGIDecodeSwapChain::GetSourceRect, direct3ddxgi.idxgidecodeswapchain_getsourcerect, dxgi1_3/IDXGIDecodeSwapChain::GetSourceRect
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
 - IDXGIDecodeSwapChain::GetSourceRect
 - dxgi1_3/IDXGIDecodeSwapChain::GetSourceRect
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
 - IDXGIDecodeSwapChain.GetSourceRect
---

# IDXGIDecodeSwapChain::GetSourceRect


## -description

Gets the source region that is used for the swap chain.

## -parameters

### -param pRect [out]

A pointer to a <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure 
        that receives the source region for the swap chain.

## -returns

This method returns S_OK on success, or it returns one of the error codes that are described in the <a href="/windows/desktop/direct3ddxgi/dxgi-error">DXGI_ERROR</a> topic.

## -see-also

<a href="/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgidecodeswapchain">IDXGIDecodeSwapChain</a>