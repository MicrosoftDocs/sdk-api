---
UID: NE:d3d11.D3D11_UAV_DIMENSION
title: D3D11_UAV_DIMENSION (d3d11.h)
description: Unordered-access view options.
helpviewer_keywords: ["9c59cfb3-b1fd-ce9f-e9c6-64b74c033e21","D3D11_UAV_DIMENSION","D3D11_UAV_DIMENSION enumeration [Direct3D 11]","D3D11_UAV_DIMENSION_BUFFER","D3D11_UAV_DIMENSION_TEXTURE1D","D3D11_UAV_DIMENSION_TEXTURE1DARRAY","D3D11_UAV_DIMENSION_TEXTURE2D","D3D11_UAV_DIMENSION_TEXTURE2DARRAY","D3D11_UAV_DIMENSION_TEXTURE3D","D3D11_UAV_DIMENSION_UNKNOWN","d3d11/D3D11_UAV_DIMENSION","d3d11/D3D11_UAV_DIMENSION_BUFFER","d3d11/D3D11_UAV_DIMENSION_TEXTURE1D","d3d11/D3D11_UAV_DIMENSION_TEXTURE1DARRAY","d3d11/D3D11_UAV_DIMENSION_TEXTURE2D","d3d11/D3D11_UAV_DIMENSION_TEXTURE2DARRAY","d3d11/D3D11_UAV_DIMENSION_TEXTURE3D","d3d11/D3D11_UAV_DIMENSION_UNKNOWN","direct3d11.d3d11_uav_dimension"]
old-location: direct3d11\d3d11_uav_dimension.htm
tech.root: direct3d11
ms.assetid: c9a2bcd1-9cfb-4cac-87eb-4747af745fdd
ms.date: 12/05/2018
ms.keywords: 9c59cfb3-b1fd-ce9f-e9c6-64b74c033e21, D3D11_UAV_DIMENSION, D3D11_UAV_DIMENSION enumeration [Direct3D 11], D3D11_UAV_DIMENSION_BUFFER, D3D11_UAV_DIMENSION_TEXTURE1D, D3D11_UAV_DIMENSION_TEXTURE1DARRAY, D3D11_UAV_DIMENSION_TEXTURE2D, D3D11_UAV_DIMENSION_TEXTURE2DARRAY, D3D11_UAV_DIMENSION_TEXTURE3D, D3D11_UAV_DIMENSION_UNKNOWN, d3d11/D3D11_UAV_DIMENSION, d3d11/D3D11_UAV_DIMENSION_BUFFER, d3d11/D3D11_UAV_DIMENSION_TEXTURE1D, d3d11/D3D11_UAV_DIMENSION_TEXTURE1DARRAY, d3d11/D3D11_UAV_DIMENSION_TEXTURE2D, d3d11/D3D11_UAV_DIMENSION_TEXTURE2DARRAY, d3d11/D3D11_UAV_DIMENSION_TEXTURE3D, d3d11/D3D11_UAV_DIMENSION_UNKNOWN, direct3d11.d3d11_uav_dimension
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
req.typenames: D3D11_UAV_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D11_UAV_DIMENSION
 - d3d11/D3D11_UAV_DIMENSION
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
 - D3D11_UAV_DIMENSION
---

# D3D11_UAV_DIMENSION enumeration


## -description

Unordered-access view options.

## -enum-fields

### -field D3D11_UAV_DIMENSION_UNKNOWN:0

The view type is unknown.

### -field D3D11_UAV_DIMENSION_BUFFER:1

View the resource as a buffer.

### -field D3D11_UAV_DIMENSION_TEXTURE1D:2

View the resource as a 1D texture.

### -field D3D11_UAV_DIMENSION_TEXTURE1DARRAY:3

View the resource as a 1D texture array.

### -field D3D11_UAV_DIMENSION_TEXTURE2D:4

View the resource as a 2D texture.

### -field D3D11_UAV_DIMENSION_TEXTURE2DARRAY:5

View the resource as a 2D texture array.

### -field D3D11_UAV_DIMENSION_TEXTURE3D:8

View the resource as a 3D texture array.

## -remarks

This enumeration is used by a unordered access-view description (see <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_unordered_access_view_desc">D3D11_UNORDERED_ACCESS_VIEW_DESC</a>).

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-core-enums">Core Enumerations</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-enums">Resource Enumerations</a>
