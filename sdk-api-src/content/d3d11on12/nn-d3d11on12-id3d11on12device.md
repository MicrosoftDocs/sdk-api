---
UID: NN:d3d11on12.ID3D11On12Device
title: ID3D11On12Device
author: windows-sdk-content
description: Handles the creation, wrapping and releasing of D3D11 resources for Direct3D 11on12.
old-location: direct3d12\id3d11on12device.htm
tech.root: direct3d12
ms.assetid: 031F9AC2-E5C0-47F9-B084-2D2431F1187A
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: ID3D11On12Device, ID3D11On12Device interface, ID3D11On12Device interface,described, d3d11on12/ID3D11On12Device, direct3d12.id3d11on12device
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11on12.h
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
req.lib: D3D11.lib
req.dll: D3D11.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.dll
api_name:
 - ID3D11On12Device
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11On12Device interface


## -description


Handles the creation, wrapping and releasing of D3D11 resources for Direct3D 11on12.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11On12Device</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>ID3D11On12Device</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11On12Device</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn913198(v=VS.85).aspx">AcquireWrappedResources</a>
</td>
<td align="left" width="63%">
Acquires D3D11 resources for use with D3D 11on12.
          Indicates that rendering to the wrapped resources can begin again.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn913199(v=VS.85).aspx">CreateWrappedResource</a>
</td>
<td align="left" width="63%">
This method creates D3D11 resources for use with D3D 11on12.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn913200(v=VS.85).aspx">ReleaseWrappedResources</a>
</td>
<td align="left" width="63%">
Releases D3D11 resources that were wrapped for D3D 11on12.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn913193(v=VS.85).aspx">11on12 Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>
 

 

