---
UID: NN:dxgi1_3.IDXGISwapChain2
title: IDXGISwapChain2 (dxgi1_3.h)
description: Extends IDXGISwapChain1 with methods to support swap back buffer scaling and lower-latency swap chains.
old-location: direct3ddxgi\idxgiswapchain2.htm
tech.root: direct3ddxgi
ms.assetid: 1E14EAF6-5EEA-4B4A-8F5F-0BC779093654
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain2, IDXGISwapChain2 interface [DXGI], IDXGISwapChain2 interface [DXGI],described, direct3ddxgi.idxgiswapchain2, dxgi1_3/IDXGISwapChain2
f1_keywords:
- dxgi1_3/IDXGISwapChain2
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGISwapChain2 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a> with methods to support swap back buffer scaling and lower-latency swap chains.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>. <b>IDXGISwapChain2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISwapChain2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject">GetFrameLatencyWaitableObject</a>
</td>
<td align="left" width="63%">
Returns a waitable handle that signals when the DXGI adapter has finished presenting a new frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform">GetMatrixTransform</a>
</td>
<td align="left" width="63%">
Gets the transform matrix that will be applied to a composition swap chain upon the next present. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency">GetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Gets the number of frames that the swap chain is allowed to queue for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize">GetSourceSize</a>
</td>
<td align="left" width="63%">
Gets the source region used for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform">SetMatrixTransform</a>
</td>
<td align="left" width="63%">
Sets the transform matrix that will be applied to a composition swap chain upon the next present. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency">SetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Sets the number of frames that the swap chain is allowed to queue for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize">SetSourceSize</a>
</td>
<td align="left" width="63%">
Sets the source region to be used for the swap chain.

</td>
</tr>
</table> 


## -remarks



You can create a swap chain by 
calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcomposition">IDXGIFactory2::CreateSwapChainForComposition</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforcorewindow">IDXGIFactory2::CreateSwapChainForCoreWindow</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgifactory2-createswapchainforhwnd">IDXGIFactory2::CreateSwapChainForHwnd</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_2/nn-dxgi1_2-idxgiswapchain1">IDXGISwapChain1</a>
 

 

