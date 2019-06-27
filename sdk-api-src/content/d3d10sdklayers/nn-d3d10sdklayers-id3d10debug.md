---
UID: NN:d3d10sdklayers.ID3D10Debug
title: ID3D10Debug (d3d10sdklayers.h)
author: windows-sdk-content
description: A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.
old-location: direct3d10\id3d10debug.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: 9243084e-1ae3-39f6-3e6b-d8150af7e0cc, ID3D10Debug, ID3D10Debug interface [Direct3D 10], ID3D10Debug interface [Direct3D 10],described, d3d10sdklayers/ID3D10Debug, direct3d10.id3d10debug
ms.topic: interface
f1_keywords: 
 - "d3d10sdklayers/ID3D10Debug"
req.header: d3d10sdklayers.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10Debug
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Debug interface


## -description


A debug interface controls debug settings, validates pipeline state and can only be used if the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-api-features-layers">debug layer</a> is turned on.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Debug</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10Debug</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D10Debug</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-getfeaturemask">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Get a bitfield of flags that indicates which debug features are on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-getpresentperrenderopdelay">GetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Get the number of milliseconds to sleep after <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-getswapchain">GetSwapChain</a>
</td>
<td align="left" width="63%">
Get the swap chain that the runtime will use for automatically calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setfeaturemask">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Set a bitfield of flags that will turn debug features on and off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setpresentperrenderopdelay">SetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Set the number of milliseconds to sleep after <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-setswapchain">SetSwapChain</a>
</td>
<td align="left" width="63%">
Set a swap chain that the runtime will use for automatically calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d10sdklayers/nf-d3d10sdklayers-id3d10debug-validate">Validate</a>
</td>
<td align="left" width="63%">
Check the validity of pipeline state.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10device">ID3D10Device Interface</a> using <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q_)">IUnknown::QueryInterface</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-core-interfaces">Core Interfaces</a>
 

 

