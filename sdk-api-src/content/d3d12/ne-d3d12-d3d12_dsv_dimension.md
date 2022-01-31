---
UID: NE:d3d12.D3D12_DSV_DIMENSION
title: D3D12_DSV_DIMENSION (d3d12.h)
description: Specifies how to access a resource used in a depth-stencil view.
helpviewer_keywords: ["D3D12_DSV_DIMENSION","D3D12_DSV_DIMENSION enumeration","D3D12_DSV_DIMENSION_TEXTURE1D","D3D12_DSV_DIMENSION_TEXTURE1DARRAY","D3D12_DSV_DIMENSION_TEXTURE2D","D3D12_DSV_DIMENSION_TEXTURE2DARRAY","D3D12_DSV_DIMENSION_TEXTURE2DMS","D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY","D3D12_DSV_DIMENSION_UNKNOWN","d3d12/D3D12_DSV_DIMENSION","d3d12/D3D12_DSV_DIMENSION_TEXTURE1D","d3d12/D3D12_DSV_DIMENSION_TEXTURE1DARRAY","d3d12/D3D12_DSV_DIMENSION_TEXTURE2D","d3d12/D3D12_DSV_DIMENSION_TEXTURE2DARRAY","d3d12/D3D12_DSV_DIMENSION_TEXTURE2DMS","d3d12/D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY","d3d12/D3D12_DSV_DIMENSION_UNKNOWN","direct3d12.d3d12_dsv_dimension"]
old-location: direct3d12\d3d12_dsv_dimension.htm
tech.root: direct3d12
ms.assetid: 87ABAD56-E5EE-4F96-87DC-D1EB485B621D
ms.date: 12/05/2018
ms.keywords: D3D12_DSV_DIMENSION, D3D12_DSV_DIMENSION enumeration, D3D12_DSV_DIMENSION_TEXTURE1D, D3D12_DSV_DIMENSION_TEXTURE1DARRAY, D3D12_DSV_DIMENSION_TEXTURE2D, D3D12_DSV_DIMENSION_TEXTURE2DARRAY, D3D12_DSV_DIMENSION_TEXTURE2DMS, D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY, D3D12_DSV_DIMENSION_UNKNOWN, d3d12/D3D12_DSV_DIMENSION, d3d12/D3D12_DSV_DIMENSION_TEXTURE1D, d3d12/D3D12_DSV_DIMENSION_TEXTURE1DARRAY, d3d12/D3D12_DSV_DIMENSION_TEXTURE2D, d3d12/D3D12_DSV_DIMENSION_TEXTURE2DARRAY, d3d12/D3D12_DSV_DIMENSION_TEXTURE2DMS, d3d12/D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY, d3d12/D3D12_DSV_DIMENSION_UNKNOWN, direct3d12.d3d12_dsv_dimension
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
req.typenames: D3D12_DSV_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DSV_DIMENSION
 - d3d12/D3D12_DSV_DIMENSION
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
 - D3D12_DSV_DIMENSION
---

# D3D12_DSV_DIMENSION enumeration


## -description

Specifies how to access a resource used in a depth-stencil view.

## -enum-fields

### -field D3D12_DSV_DIMENSION_UNKNOWN:0

<b>D3D12_DSV_DIMENSION_UNKNOWN</b> is not a valid value for <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a> and is not used.

### -field D3D12_DSV_DIMENSION_TEXTURE1D:1

The resource will be accessed as a 1D texture.

### -field D3D12_DSV_DIMENSION_TEXTURE1DARRAY:2

The resource will be accessed as an array of 1D textures.

### -field D3D12_DSV_DIMENSION_TEXTURE2D:3

The resource will be accessed as a 2D texture.

### -field D3D12_DSV_DIMENSION_TEXTURE2DARRAY:4

The resource will be accessed as an array of 2D textures.

### -field D3D12_DSV_DIMENSION_TEXTURE2DMS:5

The resource will be accessed as a 2D texture with multi sampling.

### -field D3D12_DSV_DIMENSION_TEXTURE2DMSARRAY:6

The resource will be accessed as an array of 2D textures with multi sampling.

## -remarks

Specify one of the values in this enumeration in the <b>ViewDimension</b> member of a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_depth_stencil_view_desc">D3D12_DEPTH_STENCIL_VIEW_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
