---
UID: NS:d3d10.D3D10_TEX1D_SRV
title: D3D10_TEX1D_SRV (d3d10.h)
description: Specifies the subresource from a 1D texture to use in a shader-resource view.helpviewer_keywords: ["D3D10_TEX1D_SRV","D3D10_TEX1D_SRV structure [Direct3D 10]","d3d10/D3D10_TEX1D_SRV","d4d7de7d-f574-5d27-4164-a30ae50fa54b","direct3d10.d3d10_tex1d_srv"]
old-location: direct3d10\d3d10_tex1d_srv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex1d_srv.htm
ms.date: 12/05/2018
ms.keywords: D3D10_TEX1D_SRV, D3D10_TEX1D_SRV structure [Direct3D 10], d3d10/D3D10_TEX1D_SRV, d4d7de7d-f574-5d27-4164-a30ae50fa54b, direct3d10.d3d10_tex1d_srv
f1_keywords:
- d3d10/D3D10_TEX1D_SRV
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- D3D10.h
api_name:
- D3D10_TEX1D_SRV
targetos: Windows
req.typenames: D3D10_TEX1D_SRV
req.redist: 
ms.custom: 19H1
---

# D3D10_TEX1D_SRV structure


## -description


Specifies the <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource</a> from a <a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">1D texture</a> to use in a shader-resource view.


## -struct-fields




### -field MostDetailedMip

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> -1.


### -field MipLevels

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of mipmap levels to use.


## -remarks



This structure is one member of a shader-resource-view description (see <a href="https://docs.microsoft.com/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc">D3D10_SHADER_RESOURCE_VIEW_DESC</a>).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>
 

 

