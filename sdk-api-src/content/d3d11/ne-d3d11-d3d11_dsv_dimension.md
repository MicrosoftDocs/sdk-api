---
UID: NE:d3d11.D3D11_DSV_DIMENSION
title: D3D11_DSV_DIMENSION (d3d11.h)
description: Specifies how to access a resource used in a depth-stencil view.
helpviewer_keywords: ["D3D11_DSV_DIMENSION","D3D11_DSV_DIMENSION enumeration [Direct3D 11]","D3D11_DSV_DIMENSION_TEXTURE1D","D3D11_DSV_DIMENSION_TEXTURE1DARRAY","D3D11_DSV_DIMENSION_TEXTURE2D","D3D11_DSV_DIMENSION_TEXTURE2DARRAY","D3D11_DSV_DIMENSION_TEXTURE2DMS","D3D11_DSV_DIMENSION_TEXTURE2DMSARRAY","D3D11_DSV_DIMENSION_UNKNOWN","d3d11/D3D11_DSV_DIMENSION","d3d11/D3D11_DSV_DIMENSION_TEXTURE1D","d3d11/D3D11_DSV_DIMENSION_TEXTURE1DARRAY","d3d11/D3D11_DSV_DIMENSION_TEXTURE2D","d3d11/D3D11_DSV_DIMENSION_TEXTURE2DARRAY","d3d11/D3D11_DSV_DIMENSION_TEXTURE2DMS","d3d11/D3D11_DSV_DIMENSION_TEXTURE2DMSARRAY","d3d11/D3D11_DSV_DIMENSION_UNKNOWN","direct3d11.d3d11_dsv_dimension","e1e4f45e-491d-c8b8-f372-71bce44a4547"]
old-location: direct3d11\d3d11_dsv_dimension.htm
tech.root: direct3d11
ms.assetid: 3037e940-6915-4b1d-b0ae-cd440033ac38
ms.date: 12/05/2018
ms.keywords: D3D11_DSV_DIMENSION, D3D11_DSV_DIMENSION enumeration [Direct3D 11], D3D11_DSV_DIMENSION_TEXTURE1D, D3D11_DSV_DIMENSION_TEXTURE1DARRAY, D3D11_DSV_DIMENSION_TEXTURE2D, D3D11_DSV_DIMENSION_TEXTURE2DARRAY, D3D11_DSV_DIMENSION_TEXTURE2DMS, D3D11_DSV_DIMENSION_TEXTURE2DMSARRAY, D3D11_DSV_DIMENSION_UNKNOWN, d3d11/D3D11_DSV_DIMENSION, d3d11/D3D11_DSV_DIMENSION_TEXTURE1D, d3d11/D3D11_DSV_DIMENSION_TEXTURE1DARRAY, d3d11/D3D11_DSV_DIMENSION_TEXTURE2D, d3d11/D3D11_DSV_DIMENSION_TEXTURE2DARRAY, d3d11/D3D11_DSV_DIMENSION_TEXTURE2DMS, d3d11/D3D11_DSV_DIMENSION_TEXTURE2DMSARRAY, d3d11/D3D11_DSV_DIMENSION_UNKNOWN, direct3d11.d3d11_dsv_dimension, e1e4f45e-491d-c8b8-f372-71bce44a4547
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
req.typenames: D3D11_DSV_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_DSV_DIMENSION
 - d3d11/D3D11_DSV_DIMENSION
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
 - D3D11_DSV_DIMENSION
---

# D3D11_DSV_DIMENSION enumeration


## -description

Specifies how to access a resource used in a depth-stencil view.

## -enum-fields

### -field D3D11_DSV_DIMENSION_UNKNOWN:0

<i>D3D11_DSV_DIMENSION_UNKNOWN</i> is not a valid value for <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a> and is not used.

### -field D3D11_DSV_DIMENSION_TEXTURE1D:1

The resource will be accessed as a 1D texture.

### -field D3D11_DSV_DIMENSION_TEXTURE1DARRAY:2

The resource will be accessed as an array of 1D textures.

### -field D3D11_DSV_DIMENSION_TEXTURE2D:3

The resource will be accessed as a 2D texture.

### -field D3D11_DSV_DIMENSION_TEXTURE2DARRAY:4

The resource will be accessed as an array of 2D textures.

### -field D3D11_DSV_DIMENSION_TEXTURE2DMS:5

The resource will be accessed as a 2D texture with multisampling.

### -field D3D11_DSV_DIMENSION_TEXTURE2DMSARRAY:6

The resource will be accessed as an array of 2D textures with multisampling.

## -remarks

This enumeration is used in <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_depth_stencil_view_desc">D3D11_DEPTH_STENCIL_VIEW_DESC</a> to create a depth-stencil view.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
