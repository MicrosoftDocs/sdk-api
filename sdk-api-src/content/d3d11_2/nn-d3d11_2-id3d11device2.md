---
UID: NN:d3d11_2.ID3D11Device2
title: ID3D11Device2
author: windows-sdk-content
description: The device interface represents a virtual adapter; it is used to create resources. ID3D11Device2 adds new methods to those in ID3D11Device1.
old-location: direct3d11\id3d11device2.htm
old-project: direct3d11
ms.assetid: C476AA0E-4A49-4E1E-8308-FB72EAD3E30C
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11Device2, ID3D11Device2 interface [Direct3D 11], ID3D11Device2 interface [Direct3D 11],described, d3d11_2/ID3D11Device2, direct3d11.id3d11device2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: d3d11_2.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: D3D11_TILE_RANGE_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Device2
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11Device2 interface


## -description


The device interface represents a virtual adapter; it is used to create resources. <b>ID3D11Device2</b> adds new methods to those in <a href="https://msdn.microsoft.com/en-us/library/Hh404575(v=VS.85).aspx">ID3D11Device1</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Device2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Hh404575(v=VS.85).aspx">ID3D11Device1</a>. <b>ID3D11Device2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11Device2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280494(v=VS.85).aspx">CheckMultisampleQualityLevels1</a>
</td>
<td align="left" width="63%">
Get the number of quality levels available during multisampling.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280495(v=VS.85).aspx">CreateDeferredContext2</a>
</td>
<td align="left" width="63%">
Creates a deferred context, which can record <a href="https://msdn.microsoft.com/en-us/library/Ff476885(v=VS.85).aspx">command lists</a>.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280496(v=VS.85).aspx">GetImmediateContext2</a>
</td>
<td align="left" width="63%">
Gets an immediate context, which can play back <a href="https://msdn.microsoft.com/en-us/library/Ff476885(v=VS.85).aspx">command lists</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280497(v=VS.85).aspx">GetResourceTiling</a>
</td>
<td align="left" width="63%">
Gets info about how a tiled resource is broken into tiles.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404575(v=VS.85).aspx">ID3D11Device1</a>
 

 

