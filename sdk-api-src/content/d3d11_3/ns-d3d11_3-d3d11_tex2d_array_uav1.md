---
UID: NS:d3d11_3.D3D11_TEX2D_ARRAY_UAV1
title: D3D11_TEX2D_ARRAY_UAV1 (d3d11_3.h)
description: Describes an array of unordered-access 2D texture resources. (D3D11_TEX2D_ARRAY_UAV1)
helpviewer_keywords: ["D3D11_TEX2D_ARRAY_UAV1","D3D11_TEX2D_ARRAY_UAV1 structure [Direct3D 11]","d3d11_3/D3D11_TEX2D_ARRAY_UAV1","direct3d11.d3d11_tex2d_array_uav1"]
old-location: direct3d11\d3d11_tex2d_array_uav1.htm
tech.root: direct3d11
ms.assetid: 369301BB-2B3E-43B2-A379-BFA03712A529
ms.date: 12/05/2018
ms.keywords: D3D11_TEX2D_ARRAY_UAV1, D3D11_TEX2D_ARRAY_UAV1 structure [Direct3D 11], d3d11_3/D3D11_TEX2D_ARRAY_UAV1, direct3d11.d3d11_tex2d_array_uav1
req.header: d3d11_3.h
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
req.typenames: D3D11_TEX2D_ARRAY_UAV1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_TEX2D_ARRAY_UAV1
 - d3d11_3/D3D11_TEX2D_ARRAY_UAV1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11_3.h
api_name:
 - D3D11_TEX2D_ARRAY_UAV1
---

# D3D11_TEX2D_ARRAY_UAV1 structure


## -description

Describes an array of unordered-access 2D texture resources.

## -struct-fields

### -field MipSlice

The mipmap slice index.

### -field FirstArraySlice

The zero-based index of the first array slice to be accessed.

### -field ArraySize

The number of slices in the array.

### -field PlaneSlice

The index (plane slice number) of the plane to use in an array of textures.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-structures">Resource Structures</a>
