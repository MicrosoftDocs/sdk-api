---
UID: NN:d3d11sdklayers.ID3D11Debug
title: ID3D11Debug
author: windows-driver-content
description: A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.
old-location: direct3d11\id3d11debug.htm
old-project: direct3d11
ms.assetid: 2c640295-7a91-4a7a-92d3-909d288eb0d6
ms.author: windowsdriverdev
ms.date: 4/6/2018
ms.keywords: ID3D11Debug, ID3D11Debug interface [Direct3D 11], ID3D11Debug interface [Direct3D 11],described, b037763f-251a-579c-a6cb-8e5097410d05, d3d11sdklayers/ID3D11Debug, direct3d11.id3d11debug
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11sdklayers.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: D3D11_SHADER_TRACKING_RESOURCE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D11.lib
-	D3D11.dll
api_name:
-	ID3D11Debug
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Debug interface


## -description


A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Debug</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D11Debug</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/5c70c85a-77a5-4e3b-9247-7686d43cbd1a">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Get a bitfield of flags that indicates which debug features are on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7c55f370-df9c-40d5-97d8-6e25cb9e5579">GetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Get the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/99dcdddf-dec8-497e-862a-72ef66528fa5">GetSwapChain</a>
</td>
<td align="left" width="63%">
Get the swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a4e5f3c1-8b67-488b-8476-464c5ea5abc6">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">
Report information about a device object's lifetime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60f9da61-dc97-4b6d-b187-df3605ad9336">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Set a bit field of flags that will turn debug features on and off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72489871-819a-4f75-a3ad-03f93f5c7761">SetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Set the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/554d56e7-8901-4b39-bc1e-6db6496263c8">SetSwapChain</a>
</td>
<td align="left" width="63%">
Sets a swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">IDXGISwapChain::Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8679a68-336f-4bfa-91d6-398a75b34dfb">ValidateContext</a>
</td>
<td align="left" width="63%">
Check to see if the draw pipeline state is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ddabb4f-eeed-46d4-a1d2-501180edffe0">ValidateContextForDispatch</a>
</td>
<td align="left" width="63%">
Verifies whether the dispatch pipeline state is valid.

</td>
</tr>
</table> 


## -remarks




            This interface is obtained by querying it from the <a href="https://msdn.microsoft.com/2f2559d9-1cd6-44f6-90e2-ee0f86e39f78">ID3D11Device</a> using <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a>.
          


            For more information about the debug layer, see <a href="overviews_direct3d_11_devices_layers.htm">Debug Layer</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/100cb66a-9bf5-4d0b-9f03-ad7c00e76d9d">Layer Interfaces</a>
 

 

