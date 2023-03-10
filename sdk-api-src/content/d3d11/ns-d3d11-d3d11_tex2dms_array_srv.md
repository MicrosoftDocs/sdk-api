---
UID: NS:d3d11.D3D11_TEX2DMS_ARRAY_SRV
title: D3D11_TEX2DMS_ARRAY_SRV (d3d11.h)
description: Specifies the subresources from an array of multisampled 2D textures to use in a shader-resource view.
helpviewer_keywords: ["4eeb5c82-a7a5-65c2-774b-c2c491076826","D3D11_TEX2DMS_ARRAY_SRV","D3D11_TEX2DMS_ARRAY_SRV structure [Direct3D 11]","d3d11/D3D11_TEX2DMS_ARRAY_SRV","direct3d11.d3d11_tex2dms_array_srv"]
old-location: direct3d11\d3d11_tex2dms_array_srv.htm
tech.root: direct3d11
ms.assetid: ce020ea2-4b2e-4d80-8ad2-5982cc7ee051
ms.date: 12/05/2018
ms.keywords: 4eeb5c82-a7a5-65c2-774b-c2c491076826, D3D11_TEX2DMS_ARRAY_SRV, D3D11_TEX2DMS_ARRAY_SRV structure [Direct3D 11], d3d11/D3D11_TEX2DMS_ARRAY_SRV, direct3d11.d3d11_tex2dms_array_srv
req.header: d3d11.h
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
req.typenames: D3D11_TEX2DMS_ARRAY_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2DMS_ARRAY_SRV
 - d3d11/D3D11_TEX2DMS_ARRAY_SRV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11.h
api_name:
 - D3D11_TEX2DMS_ARRAY_SRV
---

# D3D11_TEX2DMS_ARRAY_SRV structure


## -description

Specifies the subresources from an array of multisampled 2D textures to use in a shader-resource view.

## -struct-fields

### -field FirstArraySlice

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first texture to use in an array of textures.

### -field ArraySize

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of textures to use.

## -remarks

This structure is one member of a shader-resource-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc">D3D11_SHADER_RESOURCE_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>