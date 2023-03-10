---
UID: NN:dxgi1_3.IDXGISwapChain2
title: IDXGISwapChain2 (dxgi1_3.h)
description: Extends IDXGISwapChain1 with methods to support swap back buffer scaling and lower-latency swap chains.
helpviewer_keywords: ["IDXGISwapChain2","IDXGISwapChain2 interface [DXGI]","IDXGISwapChain2 interface [DXGI]","described","direct3ddxgi.idxgiswapchain2","dxgi1_3/IDXGISwapChain2"]
old-location: direct3ddxgi\idxgiswapchain2.htm
tech.root: direct3ddxgi
ms.assetid: 1E14EAF6-5EEA-4B4A-8F5F-0BC779093654
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain2, IDXGISwapChain2 interface [DXGI], IDXGISwapChain2 interface [DXGI],described, direct3ddxgi.idxgiswapchain2, dxgi1_3/IDXGISwapChain2
req.header: dxgi1_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IDXGISwapChain2
 - dxgi1_3/IDXGISwapChain2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxgi.lib
 - dxgi.dll
api_name:
 - IDXGISwapChain2
---

# IDXGISwapChain2 interface


## -description

Extends <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a> with methods to support swap back buffer scaling and lower-latency swap chains.

## -inheritance

The <b>IDXGISwapChain2</b> interface inherits from <a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>. <b>IDXGISwapChain2</b> also has these types of members:

## -remarks

You can create a swap chain by 
calling <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>



<a href="/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>
