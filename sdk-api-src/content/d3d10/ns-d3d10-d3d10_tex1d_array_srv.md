---
UID: NS:d3d10.D3D10_TEX1D_ARRAY_SRV
title: D3D10_TEX1D_ARRAY_SRV (d3d10.h)
description: Specifies the subresource(s) from an array of 1D textures to use in a shader-resource view.
helpviewer_keywords: ["1c4bb230-5609-5f26-980d-718fe120fd71","D3D10_TEX1D_ARRAY_SRV","D3D10_TEX1D_ARRAY_SRV structure [Direct3D 10]","d3d10/D3D10_TEX1D_ARRAY_SRV","direct3d10.d3d10_tex1d_array_srv"]
old-location: direct3d10\d3d10_tex1d_array_srv.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_tex1d_array_srv.htm
ms.date: 12/05/2018
ms.keywords: 1c4bb230-5609-5f26-980d-718fe120fd71, D3D10_TEX1D_ARRAY_SRV, D3D10_TEX1D_ARRAY_SRV structure [Direct3D 10], d3d10/D3D10_TEX1D_ARRAY_SRV, direct3d10.d3d10_tex1d_array_srv
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
targetos: Windows
req.typenames: D3D10_TEX1D_ARRAY_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_TEX1D_ARRAY_SRV
 - d3d10/D3D10_TEX1D_ARRAY_SRV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D10.h
api_name:
 - D3D10_TEX1D_ARRAY_SRV
---

# D3D10_TEX1D_ARRAY_SRV structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource(s)</a> from an array of <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">1D textures</a> to use in a shader-resource view.

## -struct-fields

### -field MostDetailedMip

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b> -1.

### -field MipLevels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of subtextures to access.

### -field FirstArraySlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first texture to use in an array of textures (see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">array slice</a>)

### -field ArraySize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures in the array.

## -remarks

This structure is one member of a shader-resource-view description (see <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_shader_resource_view_desc">D3D10_SHADER_RESOURCE_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>