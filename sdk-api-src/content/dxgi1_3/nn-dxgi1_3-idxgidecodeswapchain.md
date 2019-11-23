---
UID: NN:dxgi1_3.IDXGIDecodeSwapChain
title: IDXGIDecodeSwapChain (dxgi1_3.h)

description: Represents a swap chain that is used by desktop media apps to decode video data and show it on a DirectComposition surface.
old-location: direct3ddxgi\idxgidecodeswapchain.htm
tech.root: direct3ddxgi
ms.assetid: 814EDDA6-EFEA-4281-BE06-9FF8822B4927

ms.date: 12/05/2018
ms.keywords: IDXGIDecodeSwapChain, IDXGIDecodeSwapChain interface [DXGI], IDXGIDecodeSwapChain interface [DXGI],described, direct3ddxgi.idxgidecodeswapchain, dxgi1_3/IDXGIDecodeSwapChain
ms.topic: interface
f1_keywords: 
 - "dxgi1_3/IDXGIDecodeSwapChain"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dxgi.lib
 - Dxgi.dll
api_name:
 - IDXGIDecodeSwapChain
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGIDecodeSwapChain interface


## -description


Represents a swap chain that is used by desktop media apps to decode video data and show it on a <a href="https://docs.microsoft.com/windows/desktop/directcomp/reference">DirectComposition</a> surface.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDecodeSwapChain</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXGIDecodeSwapChain</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGIDecodeSwapChain</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-getcolorspace">GetColorSpace</a>
</td>
<td align="left" width="63%">
Gets the color space used by the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-getdestsize">GetDestSize</a>
</td>
<td align="left" width="63%">
Gets the size of the destination surface to use for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-getsourcerect">GetSourceRect</a>
</td>
<td align="left" width="63%">
Gets the source region that is used for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-gettargetrect">GetTargetRect</a>
</td>
<td align="left" width="63%">
Gets the rectangle that defines the target region for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-presentbuffer">PresentBuffer</a>
</td>
<td align="left" width="63%">
Presents a frame on the output adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-setcolorspace">SetColorSpace</a>
</td>
<td align="left" width="63%">
Sets the color space used by the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-setdestsize">SetDestSize</a>
</td>
<td align="left" width="63%">
Sets the size of the destination surface to use for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-setsourcerect">SetSourceRect</a>
</td>
<td align="left" width="63%">
Sets the rectangle that defines the source region for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgidecodeswapchain-settargetrect">SetTargetRect</a>
</td>
<td align="left" width="63%">
Sets the rectangle that defines the target region for the video processing blit operation.

</td>
</tr>
</table> 


## -remarks



Decode swap chains are intended for use primarily with YUV surface formats. When using decode buffers created with an RGB surface format, the <i>TargetRect</i> and <i>DestSize</i> must be set equal to the buffer dimensions. <i>SourceRect</i> cannot exceed the buffer dimensions.
      

In clone mode, the decode swap chain is only guaranteed to be shown on the primary output.
      

Decode swap chains cannot be used with dirty rects.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgifactorymedia">IDXGIFactoryMedia</a>



<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>
 

 

