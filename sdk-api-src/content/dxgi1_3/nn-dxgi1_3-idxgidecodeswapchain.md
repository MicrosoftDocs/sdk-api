---
UID: NN:dxgi1_3.IDXGIDecodeSwapChain
title: IDXGIDecodeSwapChain
author: windows-sdk-content
description: Represents a swap chain that is used by desktop media apps to decode video data and show it on a DirectComposition surface.
old-location: direct3ddxgi\idxgidecodeswapchain.htm
old-project: direct3ddxgi
ms.assetid: 814EDDA6-EFEA-4281-BE06-9FF8822B4927
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: IDXGIDecodeSwapChain, IDXGIDecodeSwapChain interface [DXGI], IDXGIDecodeSwapChain interface [DXGI],described, direct3ddxgi.idxgidecodeswapchain, dxgi1_3/IDXGIDecodeSwapChain
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DXGI_OVERLAY_SUPPORT_FLAG
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
product: Windows
targetos: Windows
req.lib: Dxgi.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGIDecodeSwapChain interface


## -description


Represents a swap chain that is used by desktop media apps to decode video data and show it on a <a href="https://msdn.microsoft.com/A220189D-8546-4352-8F6F-AC5D2192940D">DirectComposition</a> surface.
        


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGIDecodeSwapChain</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDXGIDecodeSwapChain</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3C63C75C-6395-46E8-9070-A62220FCA3B8">GetColorSpace</a>
</td>
<td align="left" width="63%">
Gets the color space used by the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/FA01A6C1-7731-4B30-845F-4C2514B6AD77">GetDestSize</a>
</td>
<td align="left" width="63%">
Gets the size of the destination surface to use for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67DD1267-997A-4D84-BC91-D124ED1E8946">GetSourceRect</a>
</td>
<td align="left" width="63%">
Gets the source region that is used for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1B42CE33-7130-433F-940F-B45D3152BB33">GetTargetRect</a>
</td>
<td align="left" width="63%">
Gets the rectangle that defines the target region for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/EFBBE24E-9BA5-40CB-B090-EE0ADA1AF07D">PresentBuffer</a>
</td>
<td align="left" width="63%">
Presents a frame on the output adapter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/DE0AA2BF-8E98-4CF4-8CC2-760AB4B8776D">SetColorSpace</a>
</td>
<td align="left" width="63%">
Sets the color space used by the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BF35FFFE-89C7-4220-9D9F-5BFFE53D3430">SetDestSize</a>
</td>
<td align="left" width="63%">
Sets the size of the destination surface to use for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E614D9C2-9AAC-4ADC-9B7B-99C47975DA07">SetSourceRect</a>
</td>
<td align="left" width="63%">
Sets the rectangle that defines the source region for the video processing blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2B3D71F9-B13B-4680-8284-41B32CA58CEE">SetTargetRect</a>
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




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/5646B34D-EB2C-4161-8FF0-67F96254AFBC">IDXGIFactoryMedia</a>



<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>
 

 

