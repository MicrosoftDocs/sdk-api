---
UID: NE:d3d10.D3D10_DSV_DIMENSION
title: D3D10_DSV_DIMENSION (d3d10.h)
description: Specifies how to access a resource used in a depth-stencil view.
helpviewer_keywords: ["88cc34ba-f05f-2845-c538-a290a7b141ee","D3D10_DSV_DIMENSION","D3D10_DSV_DIMENSION enumeration [Direct3D 10]","D3D10_DSV_DIMENSION_TEXTURE1D","D3D10_DSV_DIMENSION_TEXTURE1DARRAY","D3D10_DSV_DIMENSION_TEXTURE2D","D3D10_DSV_DIMENSION_TEXTURE2DARRAY","D3D10_DSV_DIMENSION_TEXTURE2DMS","D3D10_DSV_DIMENSION_TEXTURE2DMSARRAY","D3D10_DSV_DIMENSION_UNKNOWN","d3d10/D3D10_DSV_DIMENSION","d3d10/D3D10_DSV_DIMENSION_TEXTURE1D","d3d10/D3D10_DSV_DIMENSION_TEXTURE1DARRAY","d3d10/D3D10_DSV_DIMENSION_TEXTURE2D","d3d10/D3D10_DSV_DIMENSION_TEXTURE2DARRAY","d3d10/D3D10_DSV_DIMENSION_TEXTURE2DMS","d3d10/D3D10_DSV_DIMENSION_TEXTURE2DMSARRAY","d3d10/D3D10_DSV_DIMENSION_UNKNOWN","direct3d10.d3d10_dsv_dimension"]
old-location: direct3d10\d3d10_dsv_dimension.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_dsv_dimension.htm
ms.date: 12/05/2018
ms.keywords: 88cc34ba-f05f-2845-c538-a290a7b141ee, D3D10_DSV_DIMENSION, D3D10_DSV_DIMENSION enumeration [Direct3D 10], D3D10_DSV_DIMENSION_TEXTURE1D, D3D10_DSV_DIMENSION_TEXTURE1DARRAY, D3D10_DSV_DIMENSION_TEXTURE2D, D3D10_DSV_DIMENSION_TEXTURE2DARRAY, D3D10_DSV_DIMENSION_TEXTURE2DMS, D3D10_DSV_DIMENSION_TEXTURE2DMSARRAY, D3D10_DSV_DIMENSION_UNKNOWN, d3d10/D3D10_DSV_DIMENSION, d3d10/D3D10_DSV_DIMENSION_TEXTURE1D, d3d10/D3D10_DSV_DIMENSION_TEXTURE1DARRAY, d3d10/D3D10_DSV_DIMENSION_TEXTURE2D, d3d10/D3D10_DSV_DIMENSION_TEXTURE2DARRAY, d3d10/D3D10_DSV_DIMENSION_TEXTURE2DMS, d3d10/D3D10_DSV_DIMENSION_TEXTURE2DMSARRAY, d3d10/D3D10_DSV_DIMENSION_UNKNOWN, direct3d10.d3d10_dsv_dimension
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
req.typenames: D3D10_DSV_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D10_DSV_DIMENSION
 - d3d10/D3D10_DSV_DIMENSION
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
 - D3D10_DSV_DIMENSION
---

# D3D10_DSV_DIMENSION enumeration


## -description

Specifies how to access a resource used in a depth-stencil <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a>.

## -enum-fields

### -field D3D10_DSV_DIMENSION_UNKNOWN:0

The resource will be accessed according to its type as determined from the actual instance this enumeration is paired with when the depth-stencil view is created.

### -field D3D10_DSV_DIMENSION_TEXTURE1D:1

The resource will be accessed as a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">1D texture</a>.

### -field D3D10_DSV_DIMENSION_TEXTURE1DARRAY:2

The resource will be accessed as an array of 1D textures.

### -field D3D10_DSV_DIMENSION_TEXTURE2D:3

The resource will be accessed as a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">2D texture</a>.

### -field D3D10_DSV_DIMENSION_TEXTURE2DARRAY:4

The resource will be accessed as an array of 2D texture.

### -field D3D10_DSV_DIMENSION_TEXTURE2DMS:5

The resource will be accessed as a 2D texture with multisampling.

### -field D3D10_DSV_DIMENSION_TEXTURE2DMSARRAY:6

The resource will be accessed as an array of 2D textures with multisampling.

## -remarks

This enumeration is used in <a href="/windows/desktop/api/d3d10/ns-d3d10-d3d10_depth_stencil_view_desc">D3D10_DEPTH_STENCIL_VIEW_DESC</a> to create a depth-stencil view.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-enums">Resource Enumerations</a>
