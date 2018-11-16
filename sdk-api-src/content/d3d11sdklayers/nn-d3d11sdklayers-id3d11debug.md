---
UID: NN:d3d11sdklayers.ID3D11Debug
title: ID3D11Debug
author: windows-sdk-content
description: A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.
old-location: direct3d11\id3d11debug.htm
tech.root: direct3d11
ms.assetid: 2c640295-7a91-4a7a-92d3-909d288eb0d6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ID3D11Debug, ID3D11Debug interface [Direct3D 11], ID3D11Debug interface [Direct3D 11],described, b037763f-251a-579c-a6cb-8e5097410d05, d3d11sdklayers/ID3D11Debug, direct3d11.id3d11debug
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11Debug interface


## -description


A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Debug</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11Debug</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Ff476367(v=VS.85).aspx">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Get a bitfield of flags that indicates which debug features are on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476368(v=VS.85).aspx">GetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Get the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476369(v=VS.85).aspx">GetSwapChain</a>
</td>
<td align="left" width="63%">
Get the swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476370(v=VS.85).aspx">ReportLiveDeviceObjects</a>
</td>
<td align="left" width="63%">
Report information about a device object's lifetime.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476371(v=VS.85).aspx">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Set a bit field of flags that will turn debug features on and off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476372(v=VS.85).aspx">SetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Set the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476373(v=VS.85).aspx">SetSwapChain</a>
</td>
<td align="left" width="63%">
Sets a swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/en-us/library/Bb174576(v=VS.85).aspx">IDXGISwapChain::Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff476374(v=VS.85).aspx">ValidateContext</a>
</td>
<td align="left" width="63%">
Check to see if the draw pipeline state is valid.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Ff728740(v=VS.85).aspx">ValidateContextForDispatch</a>
</td>
<td align="left" width="63%">
Verifies whether the dispatch pipeline state is valid.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://msdn.microsoft.com/en-us/library/Ff476379(v=VS.85).aspx">ID3D11Device</a> using <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">IUnknown::QueryInterface</a>.
          

For more information about the debug layer, see <a href="https://msdn.microsoft.com/en-us/library/Ff476881(v=VS.85).aspx">Debug Layer</a>.
          

<b>Windows Phone 8:
        </b> This API is supported.
      




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>



<a href="https://msdn.microsoft.com/en-us/library/Ff476158(v=VS.85).aspx">Layer Interfaces</a>
 

 

