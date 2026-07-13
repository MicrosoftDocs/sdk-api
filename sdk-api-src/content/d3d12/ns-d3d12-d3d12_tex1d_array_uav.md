---
UID: NS:d3d12.D3D12_TEX1D_ARRAY_UAV
title: D3D12_TEX1D_ARRAY_UAV (d3d12.h)
description: Describes an array of unordered-access 1D texture resources. (D3D12_TEX1D_ARRAY_UAV)
helpviewer_keywords: ["D3D12_TEX1D_ARRAY_UAV","D3D12_TEX1D_ARRAY_UAV structure","d3d12/D3D12_TEX1D_ARRAY_UAV","direct3d12.d3d12_tex1d_array_uav"]
old-location: direct3d12\d3d12_tex1d_array_uav.htm
tech.root: direct3d12
ms.assetid: C8BB872A-4CA7-410D-83AA-4EA2A035C46F
ms.date: 12/05/2018
ms.keywords: D3D12_TEX1D_ARRAY_UAV, D3D12_TEX1D_ARRAY_UAV structure, d3d12/D3D12_TEX1D_ARRAY_UAV, direct3d12.d3d12_tex1d_array_uav
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
req.typenames: D3D12_TEX1D_ARRAY_UAV
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEX1D_ARRAY_UAV
 - d3d12/D3D12_TEX1D_ARRAY_UAV
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
 - D3D12_TEX1D_ARRAY_UAV
---

# D3D12_TEX1D_ARRAY_UAV structure


## -description

Describes an array of unordered-access 1D texture resources.

## -struct-fields

### -field MipSlice

The mipmap slice index.

### -field FirstArraySlice

The zero-based index of the first array slice to be accessed.

### -field ArraySize

The number of slices in the array.

## -remarks

Use this structure with a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure to view the resource as an array of 1D textures.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>
