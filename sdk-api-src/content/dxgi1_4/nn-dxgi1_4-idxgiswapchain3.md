---
UID: NN:dxgi1_4.IDXGISwapChain3
title: IDXGISwapChain3 (dxgi1_4.h)
author: windows-sdk-content
description: Extends IDXGISwapChain2 with methods to support getting the index of the swap chain's current back buffer and support for color space.
old-location: direct3ddxgi\idxgiswapchain3.htm
tech.root: direct3ddxgi
ms.assetid: 3B91A70D-C635-46DF-871D-F1796D4E50E7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXGISwapChain3, IDXGISwapChain3 interface [DXGI], IDXGISwapChain3 interface [DXGI],described, direct3ddxgi.idxgiswapchain3, dxgi1_4/IDXGISwapChain3
ms.topic: interface
req.header: dxgi1_4.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - IDXGISwapChain3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXGISwapChain3 interface


## -description


Extends <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a> with methods to support getting the index of the swap chain's current back buffer and support for color space.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXGISwapChain3</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>. <b>IDXGISwapChain3</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXGISwapChain3</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-checkcolorspacesupport">CheckColorSpaceSupport</a>
</td>
<td align="left" width="63%">
Checks the swap chain's support for color space.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-getcurrentbackbufferindex">GetCurrentBackBufferIndex</a>
</td>
<td align="left" width="63%">
Gets the index of the swap chain's current back buffer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-resizebuffers1">ResizeBuffers1</a>
</td>
<td align="left" width="63%">
Changes the swap chain's back buffer size, format, and number of buffers, where the swap chain was created using a D3D12 command queue as an input device.
          This should be called when the application window is resized.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_4/nf-dxgi1_4-idxgiswapchain3-setcolorspace1">SetColorSpace1</a>
</td>
<td align="left" width="63%">
Sets the color space used by the swap chain.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3ddxgi/d3d10-graphics-reference-dxgi-interfaces">DXGI Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/dxgi1_3/nn-dxgi1_3-idxgiswapchain2">IDXGISwapChain2</a>
 

 

