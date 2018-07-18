---
UID: NN:dxgi.IDXGISwapChain
title: IDXGISwapChain
author: windows-sdk-content
description: An IDXGISwapChain interface implements one or more surfaces for storing rendered data before presenting it to an output.
old-location: direct3ddxgi\idxgiswapchain.htm
old-project: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain.htm
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: 188bf6e5-9cd2-15c4-2bbd-2b3801aac81e, IDXGISwapChain, IDXGISwapChain interface [DXGI], IDXGISwapChain interface [DXGI],described, direct3ddxgi.idxgiswapchain, dxgi/IDXGISwapChain
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: DXGI_SWAP_EFFECT
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
product: Windows
targetos: Windows
req.lib: DXGI.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXGISwapChain interface


## -description


An <b>IDXGISwapChain</b> interface implements one or more <a href="https://msdn.microsoft.com/9210b966-9e9a-4cd1-ba70-6f1a9fda9d80">surfaces</a> for storing rendered data before presenting it to an output.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain</b> interface inherits from <a href="https://msdn.microsoft.com/f2f3da88-76e9-4721-bc02-b3b82b7794b8">IDXGIDeviceSubObject</a>. <b>IDXGISwapChain</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>
</td>
<td align="left" width="63%">
Accesses one of the swap-chain's back buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ebc1ec3-87f3-46bc-8516-180d28740b38">GetContainingOutput</a>
</td>
<td align="left" width="63%">
Get the output (the display monitor) that contains the majority of the client area of the target window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8265f4bf-1d4f-4117-9316-a399e028af60">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the swap chain.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/8265f4bf-1d4f-4117-9316-a399e028af60">GetDesc</a> anymore to get a description of the swap chain. Instead, use <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c02b9e3b-5d59-4ed2-b373-2097c0e46f70">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Gets performance statistics about the last render frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9ebc22d4-a9a1-4e38-98a5-953156bd2bc5">GetFullscreenState</a>
</td>
<td align="left" width="63%">
Get the state associated with full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/62da6926-0137-4531-98b7-b9f75f5f1add">GetLastPresentCount</a>
</td>
<td align="left" width="63%">
Gets the number of times  that <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a> or <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>
</td>
<td align="left" width="63%">
Presents a rendered image to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c70aaad0-e742-4ff1-9d25-80d171f3f9de">ResizeBuffers</a>
</td>
<td align="left" width="63%">

      Changes the swap chain's back buffer size, format, and number of buffers. 
      This should be called when the application window is resized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/48dbe057-9374-4123-91cb-0d7bd4ea0514">ResizeTarget</a>
</td>
<td align="left" width="63%">
Resizes the output target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4762082c-5a61-43a0-b158-a70bbec804d4">SetFullscreenState</a>
</td>
<td align="left" width="63%">
Sets the display state to windowed or full screen.

</td>
</tr>
</table> 


## -remarks



You can create a swap chain by 
calling <a href="https://msdn.microsoft.com/B78E9F87-C6B0-4078-8C59-AFB85B9C3CBD">IDXGIFactory2::CreateSwapChainForHwnd</a>, <a href="https://msdn.microsoft.com/B3AC3AEB-3449-4444-9FD3-866A3795C41F">IDXGIFactory2::CreateSwapChainForCoreWindow</a>, or <a href="https://msdn.microsoft.com/8AE13082-F8C3-422A-A111-4E91488BD1AF">IDXGIFactory2::CreateSwapChainForComposition</a>. You can also create a swap chain when you call <a href="https://msdn.microsoft.com/84d73e8c-f13c-4343-91de-57f9f8a0ad96">D3D11CreateDeviceAndSwapChain</a>; however, you can then only access the sub-set of swap-chain functionality that the <b>IDXGISwapChain</b> interface provides.




## -see-also




<a href="https://msdn.microsoft.com/b561b26b-961c-4d5e-8483-56b51b989bf7">DXGI Interfaces</a>



<a href="https://msdn.microsoft.com/f2f3da88-76e9-4721-bc02-b3b82b7794b8">IDXGIDeviceSubObject</a>
 

 

