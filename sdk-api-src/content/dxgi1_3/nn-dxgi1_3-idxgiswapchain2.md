---
UID: NN:dxgi1_3.IDXGISwapChain2
title: IDXGISwapChain2
author: windows-sdk-content
description: Extends IDXGISwapChain1 with methods to support swap back buffer scaling and lower-latency swap chains.
old-location: direct3ddxgi\idxgiswapchain2.htm
tech.root: direct3ddxgi
ms.assetid: 1E14EAF6-5EEA-4B4A-8F5F-0BC779093654
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: IDXGISwapChain2, IDXGISwapChain2 interface [DXGI], IDXGISwapChain2 interface [DXGI],described, direct3ddxgi.idxgiswapchain2, dxgi1_3/IDXGISwapChain2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain2 interface


## -description


Extends <a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a> with methods to support swap back buffer scaling and lower-latency swap chains.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain2</b> interface inherits from <a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>. <b>IDXGISwapChain2</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/70E7347F-C6F9-49FA-9796-B728CF3F7778">GetFrameLatencyWaitableObject</a>
</td>
<td align="left" width="63%">
Returns a waitable handle that signals when the DXGI adapter has finished presenting a new frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/90302283-BB0A-44A9-8CD2-591571EF74ED">GetMatrixTransform</a>
</td>
<td align="left" width="63%">
Gets the transform matrix that will be applied to a composition swap chain upon the next present. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F0A07900-8F10-475B-B13F-E0F49B50C2EB">GetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Gets the number of frames that the swap chain is allowed to queue for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C7E9BC13-74E5-4981-8F87-390F95B71AE0">GetSourceSize</a>
</td>
<td align="left" width="63%">
Gets the source region used for the swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AAED8A59-3190-49A0-93AA-F5CAF9088877">SetMatrixTransform</a>
</td>
<td align="left" width="63%">
Sets the transform matrix that will be applied to a composition swap chain upon the next present. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AF3F03F2-38B4-474A-8A66-86A93D776EA0">SetMaximumFrameLatency</a>
</td>
<td align="left" width="63%">
Sets the number of frames that the swap chain is allowed to queue for rendering.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD424F5A-9735-4E90-9FAD-A0B827D7AD80">SetSourceSize</a>
</td>
<td align="left" width="63%">
Sets the source region to be used for the swap chain.

</td>
</tr>
</table> 


## -remarks



You can create a swap chain by 
calling <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>



<a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>



<a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>



<a href="https://msdn.microsoft.com/A674E006-4323-4967-9B9B-0E3965040DBF">IDXGISwapChain1</a>
 

 

