---
UID: NS:d3d12.D3D12_TEX2DMS_ARRAY_SRV
title: D3D12_TEX2DMS_ARRAY_SRV (d3d12.h)
description: Describes the subresources from an array of multi sampled 2D textures to use in a shader-resource view.
helpviewer_keywords: ["D3D12_TEX2DMS_ARRAY_SRV","D3D12_TEX2DMS_ARRAY_SRV structure","d3d12/D3D12_TEX2DMS_ARRAY_SRV","direct3d12.d3d12_tex2dms_array_srv"]
old-location: direct3d12\d3d12_tex2dms_array_srv.htm
tech.root: direct3d12
ms.assetid: 2AA430ED-4CE8-4EBD-9541-6EE0FFBA3873
ms.date: 12/05/2018
ms.keywords: D3D12_TEX2DMS_ARRAY_SRV, D3D12_TEX2DMS_ARRAY_SRV structure, d3d12/D3D12_TEX2DMS_ARRAY_SRV, direct3d12.d3d12_tex2dms_array_srv
req.header: d3d12.h
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
req.typenames: D3D12_TEX2DMS_ARRAY_SRV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEX2DMS_ARRAY_SRV
 - d3d12/D3D12_TEX2DMS_ARRAY_SRV
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_TEX2DMS_ARRAY_SRV
---

# D3D12_TEX2DMS_ARRAY_SRV structure


## -description

Describes the subresources from an array of multi sampled 2D textures to use in a shader-resource view.

## -struct-fields

### -field FirstArraySlice

The index of the first texture to use in an array of textures.

### -field ArraySize

Number of textures to use.

## -remarks

This structure is one member of a shader-resource-view description, <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_shader_resource_view_desc">D3D12_SHADER_RESOURCE_VIEW_DESC</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>