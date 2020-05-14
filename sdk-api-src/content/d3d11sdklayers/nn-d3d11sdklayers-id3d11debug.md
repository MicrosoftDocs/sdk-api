---
UID: NN:d3d11sdklayers.ID3D11Debug
title: ID3D11Debug (d3d11sdklayers.h)
description: A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.helpviewer_keywords: ["ID3D11Debug","ID3D11Debug interface [Direct3D 11]","ID3D11Debug interface [Direct3D 11]","described","b037763f-251a-579c-a6cb-8e5097410d05","d3d11sdklayers/ID3D11Debug","direct3d11.id3d11debug"]
old-location: direct3d11\id3d11debug.htm
tech.root: direct3d11
ms.assetid: 2c640295-7a91-4a7a-92d3-909d288eb0d6
ms.date: 12/05/2018
ms.keywords: ID3D11Debug, ID3D11Debug interface [Direct3D 11], ID3D11Debug interface [Direct3D 11],described, b037763f-251a-579c-a6cb-8e5097410d05, d3d11sdklayers/ID3D11Debug, direct3d11.id3d11debug
f1_keywords:
- d3d11sdklayers/ID3D11Debug
dev_langs:
- c++
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- D3D11.lib
- D3D11.dll
api_name:
- ID3D11Debug
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D11Debug interface


## -description


A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Debug</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Debug</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3D11Debug</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-getfeaturemask">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Get a bitfield of flags that indicates which debug features are on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-getpresentperrenderopdelay">GetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Get the number of milliseconds to sleep after <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-getswapchain">GetSwapChain</a>
</td>
<td align="left" width="63%">
Get the swap chain that the runtime will use for automatically calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-reportlivedeviceobjects">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">
Report information about a device object's lifetime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setfeaturemask">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Set a bit field of flags that will turn debug features on and off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setpresentperrenderopdelay">SetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Set the number of milliseconds to sleep after <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-setswapchain">SetSwapChain</a>
</td>
<td align="left" width="63%">
Sets a swap chain that the runtime will use for automatically calling <a href="https://docs.microsoft.com/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present">IDXGISwapChain::Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-validatecontext">ValidateContext</a>
</td>
<td align="left" width="63%">
Check to see if the draw pipeline state is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11sdklayers/nf-d3d11sdklayers-id3d11debug-validatecontextfordispatch">ValidateContextForDispatch</a>
</td>
<td align="left" width="63%">
Verifies whether the dispatch pipeline state is valid.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://docs.microsoft.com/windows/desktop/api/d3d11/nn-d3d11-id3d11device">ID3D11Device</a> using <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a>.
          

For more information about the debug layer, see <a href="https://docs.microsoft.com/windows/desktop/direct3d11/overviews-direct3d-11-devices-layers">Debug Layer</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-layer-interfaces">Layer Interfaces</a>
 

 

