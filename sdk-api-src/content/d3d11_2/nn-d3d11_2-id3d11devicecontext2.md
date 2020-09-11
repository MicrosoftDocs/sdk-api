---
UID: NN:d3d11_2.ID3D11DeviceContext2
title: ID3D11DeviceContext2 (d3d11_2.h)
description: The device context interface represents a device context; it is used to render commands. ID3D11DeviceContext2 adds new methods to those in ID3D11DeviceContext1.
helpviewer_keywords: ["ID3D11DeviceContext2","ID3D11DeviceContext2 interface [Direct3D 11]","ID3D11DeviceContext2 interface [Direct3D 11]","described","d3d11_2/ID3D11DeviceContext2","direct3d11.id3d11devicecontext2"]
old-location: direct3d11\id3d11devicecontext2.htm
tech.root: direct3d11
ms.assetid: 8B6B6F6E-9236-4DEE-A1BA-5FE45736DFAA
ms.date: 12/05/2018
ms.keywords: ID3D11DeviceContext2, ID3D11DeviceContext2 interface [Direct3D 11], ID3D11DeviceContext2 interface [Direct3D 11],described, d3d11_2/ID3D11DeviceContext2, direct3d11.id3d11devicecontext2
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11DeviceContext2
 - d3d11_2/ID3D11DeviceContext2
dev_langs:
 - c++
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
---

# ID3D11DeviceContext2 interface


## -description

The device context interface represents a device context; it is used to render commands. <b>ID3D11DeviceContext2</b> adds new methods to those in <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11DeviceContext2</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>. <b>ID3D11DeviceContext2</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-updatetiles">	UpdateTiles</a>
</td>
<td align="left" width="63%">
Updates tiles by copying from app memory to the tiled resource. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-begineventint">BeginEventInt</a>
</td>
<td align="left" width="63%">
Allows applications to annotate the beginning of a range of graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytilemappings">CopyTileMappings</a>
</td>
<td align="left" width="63%">
Copies mappings from a source tiled resource to a destination tiled resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-copytiles">CopyTiles</a>
</td>
<td align="left" width="63%">
Copies tiles from buffer to tiled resource or vice versa. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-endevent">EndEvent</a>
</td>
<td align="left" width="63%">
Allows applications to annotate the end of a range of graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-isannotationenabled">IsAnnotationEnabled</a>
</td>
<td align="left" width="63%">
Allows apps to determine when either a capture or profiling request is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool">ResizeTilePool</a>
</td>
<td align="left" width="63%">
Resizes a tile pool.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-setmarkerint">SetMarkerInt</a>
</td>
<td align="left" width="63%">
Allows applications to annotate graphics commands.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-tiledresourcebarrier">TiledResourceBarrier</a>
</td>
<td align="left" width="63%">
Specifies a data access ordering constraint between multiple tiled resources.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_2/nf-d3d11_2-id3d11devicecontext2-updatetilemappings">UpdateTileMappings</a>
</td>
<td align="left" width="63%">
Updates mappings of tile locations in tiled resources to memory locations in a tile pool.

</td>
</tr>
</table>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-interfaces">Core Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11devicecontext1">ID3D11DeviceContext1</a>

