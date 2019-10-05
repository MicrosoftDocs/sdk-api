---
UID: NF:d3d10.ID3D10Texture3D.Unmap
title: ID3D10Texture3D::Unmap (d3d10.h)
author: windows-sdk-content
description: Invalidate the pointer to the resource retrieved by ID3D10Texture3D::Map, and re-enable the GPU's access to the resource.
old-location: direct3d10\id3d10texture3d_unmap.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture3d_unmap.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ID3D10Texture3D interface [Direct3D 10],Unmap method, ID3D10Texture3D.Unmap, ID3D10Texture3D::Unmap, Unmap, Unmap method [Direct3D 10], Unmap method [Direct3D 10],ID3D10Texture3D interface, c26b8025-823a-b16b-6cb8-9316b5866e7e, d3d10/ID3D10Texture3D::Unmap, direct3d10.id3d10texture3d_unmap
ms.topic: method
f1_keywords: 
 - "d3d10/ID3D10Texture3D.Unmap"
dev_langs:
 - c++
req.header: d3d10.h
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
 - ID3D10Texture3D.Unmap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Texture3D::Unmap


## -description


Invalidate the pointer to the resource retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture3d-map">ID3D10Texture3D::Map</a>, and re-enable the GPU's access to the resource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Subresource</a> to be unmapped. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-d3d10calcsubresource">D3D10CalcSubresource</a> for more details.


## -returns



Returns nothing.




## -remarks



A subresource must be mapped before Unmap is called.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Unmap() in Direct3D 10 is analogous to resource Unlock() in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10texture3d">ID3D10Texture3D Interface</a>
 

 

