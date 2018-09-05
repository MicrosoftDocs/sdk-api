---
UID: NN:d3d11_2.ID3D11DeviceContext2
title: ID3D11DeviceContext2
author: windows-sdk-content
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext2 adds new methods to those in ID3D11DeviceContext1.
old-location: direct3d11\id3d11devicecontext2.htm
old-project: direct3d11
ms.assetid: 8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ID3D11DeviceContext2, ID3D11DeviceContext2 interface [Direct3D 11], ID3D11DeviceContext2 interface [Direct3D 11],described, d3d11_2/ID3D11DeviceContext2, direct3d11.id3d11devicecontext2
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
 - ID3D11DeviceContext2
product: Windows
targetos: Windows
req.lib: D3D11.lib
req.dll: 
req.irql: 
---

# ID3D11DeviceContext2 interface


## -description


The device context interface represents a device context; it is used to render commands. <b>ID3D11DeviceContext2</b> adds new methods to those in <a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext2</b> interface inherits from <a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>. <b>ID3D11DeviceContext2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
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
<a href="https://msdn.microsoft.com/EB0F9CBD-29B2-484D-8923-6686C73487F7">	UpdateTiles</a>
</td>
<td align="left" width="63%">
Updates tiles by copying from app memory to the tiled resource. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a45e16f-a598-4196-ad9c-8a157ae94de0">BeginEventInt</a>
</td>
<td align="left" width="63%">
Allows applications to annotate the beginning of a range of graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03EBF4F5-CEC3-485D-8124-AAB90DA4D6E1">CopyTileMappings</a>
</td>
<td align="left" width="63%">
Copies mappings from a source tiled resource to a destination tiled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/C336B0C7-DB99-466C-B689-5D6634EE0B36">CopyTiles</a>
</td>
<td align="left" width="63%">
Copies tiles from buffer to tiled resource or vice versa. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1684ee4b-637d-4764-bb69-6ebc5c2985f1">EndEvent</a>
</td>
<td align="left" width="63%">
Allows applications to annotate the end of a range of graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/76096836-ab68-468e-a54a-a93ecb0bdb88">IsAnnotationEnabled</a>
</td>
<td align="left" width="63%">
Allows apps to determine when either a capture or profiling request is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0F464025-7BF3-47C4-BD77-B4C312E53B07">ResizeTilePool</a>
</td>
<td align="left" width="63%">
Resizes a tile pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bb814f16-ca58-46ad-88eb-1c67b17d0c86">SetMarkerInt</a>
</td>
<td align="left" width="63%">
Allows applications to annotate graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/D53A4336-53D8-4264-9A9B-B775AA026939">TiledResourceBarrier</a>
</td>
<td align="left" width="63%">
Specifies a data access ordering constraint between multiple tiled resources.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/542735C4-BFDE-4EA9-9595-BA30BD06422B">UpdateTileMappings</a>
</td>
<td align="left" width="63%">
Updates mappings of tile locations in tiled resources to memory locations in a tile pool.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/e96804db-0987-49ca-b1b1-321f36c13024">Core Interfaces</a>



<a href="https://msdn.microsoft.com/DD2A556D-AEF0-407E-A497-CF17ACDEB1A7">ID3D11DeviceContext1</a>
 

 

