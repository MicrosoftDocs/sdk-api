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
f1_keywords:
- dxgi/IDXGISwapChain
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGISwapChain interface


## -description


An <b>IDXGISwapChain</b> interface implements one or more <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgisurface">surfaces</a> for storing rendered data before presenting it to an output.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>. <b>IDXGISwapChain</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISwapChain</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getbuffer">GetBuffer</a>
</td>
<td align="left" width="63%">
Accesses one of the swap-chain's back buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getcontainingoutput">GetContainingOutput</a>
</td>
<td align="left" width="63%">
Get the output (the display monitor) that contains the majority of the client area of the target window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getdesc">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the swap chain.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getdesc">GetDesc</a> anymore to get a description of the swap chain. Instead, use <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-getdesc1">IDXGISwapChain1::GetDesc1</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getframestatistics">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Gets performance statistics about the last render frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getfullscreenstate">GetFullscreenState</a>
</td>
<td align="left" width="63%">
Get the state associated with full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-getlastpresentcount">GetLastPresentCount</a>
</td>
<td align="left" width="63%">
Gets the number of times  that <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> or <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1">IDXGISwapChain1::Present1</a> has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>
</td>
<td align="left" width="63%">
Presents a rendered image to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizebuffers">ResizeBuffers</a>
</td>
<td align="left" width="63%">
Changes the swap chain's back buffer size, format, and number of buffers. 
      This should be called when the application window is resized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-resizetarget">ResizeTarget</a>
</td>
<td align="left" width="63%">
Resizes the output target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-setfullscreenstate">SetFullscreenState</a>
</td>
<td align="left" width="63%">
Sets the display state to windowed or full screen.

</td>
</tr>
</table> 


## -remarks



You can create a swap chain by 
calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>. You can also create a swap chain when you call <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nf-d3d11-d3d11createdeviceandswapchain">D3D11CreateDeviceAndSwapChain</a>; however, you can then only access the sub-set of swap-chain functionality that the <b>IDXGISwapChain</b> interface provides.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nn-dxgi-idxgidevicesubobject">IDXGIDeviceSubObject</a>
 

 

