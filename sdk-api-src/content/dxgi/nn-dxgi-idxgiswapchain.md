---
UID: NN:dxgi.IDXGISwapChain
title: IDXGISwapChain
author: windows-sdk-content
description: An IDXGISwapChain interface implements one or more surfaces for storing rendered data before presenting it to an output.
old-location: direct3ddxgi\idxgiswapchain.htm
tech.root: direct3ddxgi
ms.assetid: VS|directx_sdk|~\idxgiswapchain.htm
ms.author: windowssdkdev
ms.date: 10/30/2018
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDXGISwapChain interface


## -description


An <b>IDXGISwapChain</b> interface implements one or more <a href="https://msdn.microsoft.com/en-us/library/Bb174565(v=VS.85).aspx">surfaces</a> for storing rendered data before presenting it to an output.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Bb174528(v=VS.85).aspx">IDXGIDeviceSubObject</a>. <b>IDXGISwapChain</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/Bb174570(v=VS.85).aspx">GetBuffer</a>
</td>
<td align="left" width="63%">
Accesses one of the swap-chain's back buffers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174571(v=VS.85).aspx">GetContainingOutput</a>
</td>
<td align="left" width="63%">
Get the output (the display monitor) that contains the majority of the client area of the target window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174572(v=VS.85).aspx">GetDesc</a>
</td>
<td align="left" width="63%">
Get a description of the swap chain.

<div class="alert"><b>Note</b>  Starting with Direct3D 11.1, we recommend not to use <a href="https://msdn.microsoft.com/en-us/library/Bb174572(v=VS.85).aspx">GetDesc</a> anymore to get a description of the swap chain. Instead, use <a href="https://msdn.microsoft.com/86BB75A7-C289-4EBA-A9EE-ED4F5C590BA2">IDXGISwapChain1::GetDesc1</a>.</div>
<div> </div>
</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174573(v=VS.85).aspx">GetFrameStatistics</a>
</td>
<td align="left" width="63%">
Gets performance statistics about the last render frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174574(v=VS.85).aspx">GetFullscreenState</a>
</td>
<td align="left" width="63%">
Get the state associated with full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174575(v=VS.85).aspx">GetLastPresentCount</a>
</td>
<td align="left" width="63%">
Gets the number of times  that <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> or <a href="https://msdn.microsoft.com/F795A719-71BA-4A25-B41A-9D93F96B6CA4">IDXGISwapChain1::Present1</a> has been called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">Present</a>
</td>
<td align="left" width="63%">
Presents a rendered image to the user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174577(v=VS.85).aspx">ResizeBuffers</a>
</td>
<td align="left" width="63%">
Changes the swap chain's back buffer size, format, and number of buffers. 
      This should be called when the application window is resized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174578(v=VS.85).aspx">ResizeTarget</a>
</td>
<td align="left" width="63%">
Resizes the output target.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb174579(v=VS.85).aspx">SetFullscreenState</a>
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



<a href="https://msdn.microsoft.com/en-us/library/Bb174528(v=VS.85).aspx">IDXGIDeviceSubObject</a>
 

 

