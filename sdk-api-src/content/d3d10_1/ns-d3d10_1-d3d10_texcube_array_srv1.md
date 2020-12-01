---
UID: NS:d3d10_1.D3D10_TEXCUBE_ARRAY_SRV1
title: D3D10_TEXCUBE_ARRAY_SRV1 (d3d10_1.h)
description: Specifies the subresource(s) from an array of cube textures to use in a shader-resource view.
helpviewer_keywords: ["7e56cb00-6357-582e-88ab-2d9d2918ebce","D3D10_TEXCUBE_ARRAY_SRV1","D3D10_TEXCUBE_ARRAY_SRV1 structure [Direct3D 10]","d3d10_1/D3D10_TEXCUBE_ARRAY_SRV1","direct3d10.d3d10_texcube_array_srv1"]
old-location: direct3d10\d3d10_texcube_array_srv1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_texcube_array_srv1.htm
ms.date: 12/05/2018
ms.keywords: 7e56cb00-6357-582e-88ab-2d9d2918ebce, D3D10_TEXCUBE_ARRAY_SRV1, D3D10_TEXCUBE_ARRAY_SRV1 structure [Direct3D 10], d3d10_1/D3D10_TEXCUBE_ARRAY_SRV1, direct3d10.d3d10_texcube_array_srv1
req.header: d3d10_1.h
req.include-header: D3D10_1Shader.h
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
req.typenames: D3D10_TEXCUBE_ARRAY_SRV1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_TEXCUBE_ARRAY_SRV1
 - d3d10_1/D3D10_TEXCUBE_ARRAY_SRV1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10_1.h
api_name:
 - D3D10_TEXCUBE_ARRAY_SRV1
---

# D3D10_TEXCUBE_ARRAY_SRV1 structure


## -description

Specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresource(s)</a> from an array of <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">cube textures</a> to use in a shader-resource view.

## -struct-fields

### -field MostDetailedMip

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the most detailed mipmap level to use; this number is between 0 and <b>MipLevels</b>.

### -field MipLevels

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of mipmap levels to use.

### -field First2DArrayFace

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Index of the first 2D texture to use.

### -field NumCubes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of cube textures in the array.

## -remarks

This structure is one member of a shader-resource-view description (see <a href="/windows/desktop/api/d3d10_1/ns-d3d10_1-d3d10_shader_resource_view_desc1">D3D10_SHADER_RESOURCE_VIEW_DESC1</a>).

This structure requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures">Resource Structures</a>