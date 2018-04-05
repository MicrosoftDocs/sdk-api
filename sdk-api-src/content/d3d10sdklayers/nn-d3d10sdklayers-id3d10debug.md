---
UID: NN:d3d10sdklayers.ID3D10Debug
title: ID3D10Debug
author: windows-driver-content
description: A debug interface controls debug settings, validates pipeline state and can only be used if the debug layer is turned on.
old-location: direct3d10\id3d10debug.htm
old-project: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10debug.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: 9243084e-1ae3-39f6-3e6b-d8150af7e0cc, ID3D10Debug, ID3D10Debug interface [Direct3D 10], ID3D10Debug interface [Direct3D 10], described, d3d10sdklayers/ID3D10Debug, direct3d10.id3d10debug
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: D3D10_MESSAGE_SEVERITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	D3D10.lib
-	D3D10.dll
api_name:
-	ID3D10Debug
product: Windows
targetos: Windows
req.lib: D3D10.lib
req.dll: 
req.irql: 
---

# ID3D10Debug interface


## -description


A debug interface controls debug settings, validates pipeline state and can only be used if the <a href="https://msdn.microsoft.com/19c81383-6ac7-49ea-98a3-bf761a32ab40">debug layer</a> is turned on.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D10Debug</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ID3D10Debug</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f90d8b91-b927-4c96-8b97-ee1907edd1e9">GetFeatureMask</a>
</td>
<td align="left" width="63%">
Get a bitfield of flags that indicates which debug features are on or off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3b2bcc2-3a45-4a82-a802-17d879782028">GetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Get the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31491c9c-c78b-4564-8880-08645172c5ec">GetSwapChain</a>
</td>
<td align="left" width="63%">
Get the swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e9404531-fdf4-48e0-9ab5-f4e5b32ae077">SetFeatureMask</a>
</td>
<td align="left" width="63%">
Set a bitfield of flags that will turn debug features on and off.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc724ab0-1f85-4c87-950a-3202757ba100">SetPresentPerRenderOpDelay</a>
</td>
<td align="left" width="63%">
Set the number of milliseconds to sleep after <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a> is called.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32efd1f4-92be-42e2-9922-15acc7df39a4">SetSwapChain</a>
</td>
<td align="left" width="63%">
Set a swap chain that the runtime will use for automatically calling <a href="https://msdn.microsoft.com/4214fa05-d876-420e-a125-c68d6c4e6801">Present</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a0a641ea-c7bc-4d2f-813c-d30782edd90a">Validate</a>
</td>
<td align="left" width="63%">
Check the validity of pipeline state.

</td>
</tr>
</table> 


## -remarks



This interface is obtained by querying it from the <a href="https://msdn.microsoft.com/63c7fca3-5575-41a7-9bdf-2582e6b9c182">ID3D10Device Interface</a> using <a href="http://msdn.microsoft.com/en-us/library/ms682521(VS.85).aspx">IUnknown::QueryInterface</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5ad2db8-da90-4bcd-83a7-7466723a9c3c">Core Interfaces</a>
 

 

