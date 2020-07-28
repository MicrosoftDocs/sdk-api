---
UID: NF:d3d10.ID3D10Texture2D.Unmap
title: ID3D10Texture2D::Unmap (d3d10.h)
description: Invalidate the pointer to the resource that was retrieved by ID3D10Texture2D::Map, and re-enable GPU access to the resource.
helpviewer_keywords: ["ID3D10Texture2D interface [Direct3D 10]","Unmap method","ID3D10Texture2D.Unmap","ID3D10Texture2D::Unmap","Unmap","Unmap method [Direct3D 10]","Unmap method [Direct3D 10]","ID3D10Texture2D interface","d3d10/ID3D10Texture2D::Unmap","direct3d10.id3d10texture2d_unmap","e1ca6720-deda-a569-77bf-8e1b691dd284"]
old-location: direct3d10\id3d10texture2d_unmap.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture2d_unmap.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Texture2D interface [Direct3D 10],Unmap method, ID3D10Texture2D.Unmap, ID3D10Texture2D::Unmap, Unmap, Unmap method [Direct3D 10], Unmap method [Direct3D 10],ID3D10Texture2D interface, d3d10/ID3D10Texture2D::Unmap, direct3d10.id3d10texture2d_unmap, e1ca6720-deda-a569-77bf-8e1b691dd284
f1_keywords:
- d3d10/ID3D10Texture2D.Unmap
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
- ID3D10Texture2D.Unmap
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ID3D10Texture2D::Unmap


## -description


Invalidate the pointer to the resource that was retrieved by <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-id3d10texture2d-map">ID3D10Texture2D::Map</a>, and re-enable GPU access to the resource.


## -parameters




### -param Subresource [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>


<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">Subresource</a> to be unmapped. See <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nf-d3d10-d3d10calcsubresource">D3D10CalcSubresource</a> for more details.


## -remarks



A subresource must be mapped before Unmap is called.

<table>
<tr>
<td>
Differences between Direct3D 9 and Direct3D 10:

Unmap in Direct3D 10 is analogous to resource Unlock in Direct3D 9.

</td>
</tr>
</table>
 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/d3d10/nn-d3d10-id3d10texture2d">ID3D10Texture2D Interface</a>
 

 

