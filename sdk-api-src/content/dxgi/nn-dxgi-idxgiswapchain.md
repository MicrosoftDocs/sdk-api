---
UID: NN:dxgi.IDXGISwapChain
title: IDXGISwapChain (dxgi.h)
description: An IDXGISwapChain interface implements one or more surfaces for storing rendered data before presenting it to an output.
helpviewer_keywords: ["188bf6e5-9cd2-15c4-2bbd-2b3801aac81e","IDXGISwapChain","IDXGISwapChain interface [DXGI]","IDXGISwapChain interface [DXGI]","described","direct3ddxgi.idxgiswapchain","dxgi/IDXGISwapChain"]
old-location: direct3ddxgi\idxgiswapchain.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain.htm
ms.date: 12/05/2018
ms.keywords: 188bf6e5-9cd2-15c4-2bbd-2b3801aac81e, IDXGISwapChain, IDXGISwapChain interface [DXGI], IDXGISwapChain interface [DXGI],described, direct3ddxgi.idxgiswapchain, dxgi/IDXGISwapChain
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
 - IDXGISwapChain
 - dxgi/IDXGISwapChain
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
 - IDXGISwapChain
---

# IDXGISwapChain interface


## -description

An <b>IDXGISwapChain</b> interface implements one or more <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">surfaces</a> for storing rendered data before presenting it to an output.

## -inheritance

The <b>IDXGISwapChain</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>. <b>IDXGISwapChain</b> also has these types of members:

## -remarks

You can create a swap chain by 
calling <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>. You can also create a swap chain when you call <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>; however, you can then only access the sub-set of swap-chain functionality that the <b>IDXGISwapChain</b> interface provides.

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>
