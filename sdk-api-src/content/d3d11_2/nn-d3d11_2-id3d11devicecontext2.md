---
UID: NN:d3d11_2.ID3D11DeviceContext2
title: ID3D11DeviceContext2
author: windows-sdk-content
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext2 adds new methods to those in ID3D11DeviceContext1.
old-location: direct3d11\id3d11devicecontext2.htm
tech.root: direct3d11
ms.assetid: 8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ID3D11DeviceContext2, ID3D11DeviceContext2 interface [Direct3D 11], ID3D11DeviceContext2 interface [Direct3D 11],described, d3d11_2/ID3D11DeviceContext2, direct3d11.id3d11devicecontext2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: d3d11_2.h
req.include-header: 
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
 - ID3D11DeviceContext2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D11DeviceContext2 interface


## -description


The device context interface represents a device context; it is used to render commands. <b>ID3D11DeviceContext2</b> adds new methods to those in <a href="https://msdn.microsoft.com/en-us/library/Hh404598(v=VS.85).aspx">ID3D11DeviceContext1</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext2</b> interface inherits from <a href="https://msdn.microsoft.com/en-us/library/Hh404598(v=VS.85).aspx">ID3D11DeviceContext1</a>. <b>ID3D11DeviceContext2</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>ID3D11DeviceContext2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280509(v=VS.85).aspx">	UpdateTiles</a>
</td>
<td align="left" width="63%">
Updates tiles by copying from app memory to the tiled resource. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280499(v=VS.85).aspx">BeginEventInt</a>
</td>
<td align="left" width="63%">
Allows applications to annotate the beginning of a range of graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280500(v=VS.85).aspx">CopyTileMappings</a>
</td>
<td align="left" width="63%">
Copies mappings from a source tiled resource to a destination tiled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280501(v=VS.85).aspx">CopyTiles</a>
</td>
<td align="left" width="63%">
Copies tiles from buffer to tiled resource or vice versa. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280502(v=VS.85).aspx">EndEvent</a>
</td>
<td align="left" width="63%">
Allows applications to annotate the end of a range of graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280504(v=VS.85).aspx">IsAnnotationEnabled</a>
</td>
<td align="left" width="63%">
Allows apps to determine when either a capture or profiling request is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280505(v=VS.85).aspx">ResizeTilePool</a>
</td>
<td align="left" width="63%">
Resizes a tile pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280506(v=VS.85).aspx">SetMarkerInt</a>
</td>
<td align="left" width="63%">
Allows applications to annotate graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280507(v=VS.85).aspx">TiledResourceBarrier</a>
</td>
<td align="left" width="63%">
Specifies a data access ordering constraint between multiple tiled resources.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dn280508(v=VS.85).aspx">UpdateTileMappings</a>
</td>
<td align="left" width="63%">
Updates mappings of tile locations in tiled resources to memory locations in a tile pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ff476154(v=VS.85).aspx">Core Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh404598(v=VS.85).aspx">ID3D11DeviceContext1</a>
 

 

