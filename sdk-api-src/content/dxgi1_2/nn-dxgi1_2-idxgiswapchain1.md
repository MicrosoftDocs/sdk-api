---
UID: NN:dxgi1_2.IDXGISwapChain1
title: IDXGISwapChain1 (dxgi1_2.h)
description: Provides presentation capabilities that are enhanced from IDXGISwapChain. These presentation capabilities consist of specifying dirty rectangles and scroll rectangle to optimize the presentation.
helpviewer_keywords: ["IDXGISwapChain1","IDXGISwapChain1 interface [DXGI]","IDXGISwapChain1 interface [DXGI]","described","direct3ddxgi.idxgiswapchain1","dxgi1_2/IDXGISwapChain1"]
old-location: direct3ddxgi\idxgiswapchain1.htm
tech.root: direct3ddxgi
ms.assetid: A674E006-4323-4967-9B9B-0E3965040DBF
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain1, IDXGISwapChain1 interface [DXGI], IDXGISwapChain1 interface [DXGI],described, direct3ddxgi.idxgiswapchain1, dxgi1_2/IDXGISwapChain1
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
 - IDXGISwapChain1
 - dxgi1_2/IDXGISwapChain1
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
 - IDXGISwapChain1
---

# IDXGISwapChain1 interface


## -description

Provides presentation capabilities that are enhanced from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>. These presentation capabilities consist of specifying dirty rectangles and scroll rectangle to optimize the presentation.

## -inheritance

The <b>IDXGISwapChain1</b> interface inherits from <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>. <b>IDXGISwapChain1</b> also has these types of members:

## -remarks

You can create a swap chain by 
calling <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>. You can also create a swap chain when you call <a href="/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>; however, you can then only access the sub-set of swap-chain functionality that the <a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a> interface provides.

<b>IDXGISwapChain1</b> provides the <a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-istemporarymonosupported">IsTemporaryMonoSupported</a> method that you can use to determine whether the swap chain supports "temporary mono” presentation. This type of swap chain is a stereo swap chain that can be used to present mono content.


<div class="alert"><b>Note</b>  Some stereo features like the advanced presentation flags are not represented by an explicit interface change.  Furthermore, the original (<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>) and new (<b>IDXGISwapChain1</b>) swap chain interfaces generally have the same behavior. For information about how <b>IDXGISwapChain</b> methods are translated into <b>IDXGISwapChain1</b> methods, see the descriptions of the <b>IDXGISwapChain1</b> methods.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>



<a href="/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>



<a href="/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain">IDXGISwapChain</a>
