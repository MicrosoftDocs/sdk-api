---
UID: NE:d3d12.D3D12_UAV_DIMENSION
title: D3D12_UAV_DIMENSION (d3d12.h)
description: Identifies unordered-access view options.
helpviewer_keywords: ["D3D12_UAV_DIMENSION","D3D12_UAV_DIMENSION enumeration","D3D12_UAV_DIMENSION_BUFFER","D3D12_UAV_DIMENSION_TEXTURE1D","D3D12_UAV_DIMENSION_TEXTURE1DARRAY","D3D12_UAV_DIMENSION_TEXTURE2D","D3D12_UAV_DIMENSION_TEXTURE2DARRAY","D3D12_UAV_DIMENSION_TEXTURE3D","D3D12_UAV_DIMENSION_UNKNOWN","d3d12/D3D12_UAV_DIMENSION","d3d12/D3D12_UAV_DIMENSION_BUFFER","d3d12/D3D12_UAV_DIMENSION_TEXTURE1D","d3d12/D3D12_UAV_DIMENSION_TEXTURE1DARRAY","d3d12/D3D12_UAV_DIMENSION_TEXTURE2D","d3d12/D3D12_UAV_DIMENSION_TEXTURE2DARRAY","d3d12/D3D12_UAV_DIMENSION_TEXTURE3D","d3d12/D3D12_UAV_DIMENSION_UNKNOWN","direct3d12.d3d12_uav_dimension"]
old-location: direct3d12\d3d12_uav_dimension.htm
tech.root: direct3d12
ms.assetid: 2D4DA7D4-8AC6-4507-BCC2-FB5C5431BB73
ms.date: 12/05/2018
ms.keywords: D3D12_UAV_DIMENSION, D3D12_UAV_DIMENSION enumeration, D3D12_UAV_DIMENSION_BUFFER, D3D12_UAV_DIMENSION_TEXTURE1D, D3D12_UAV_DIMENSION_TEXTURE1DARRAY, D3D12_UAV_DIMENSION_TEXTURE2D, D3D12_UAV_DIMENSION_TEXTURE2DARRAY, D3D12_UAV_DIMENSION_TEXTURE3D, D3D12_UAV_DIMENSION_UNKNOWN, d3d12/D3D12_UAV_DIMENSION, d3d12/D3D12_UAV_DIMENSION_BUFFER, d3d12/D3D12_UAV_DIMENSION_TEXTURE1D, d3d12/D3D12_UAV_DIMENSION_TEXTURE1DARRAY, d3d12/D3D12_UAV_DIMENSION_TEXTURE2D, d3d12/D3D12_UAV_DIMENSION_TEXTURE2DARRAY, d3d12/D3D12_UAV_DIMENSION_TEXTURE3D, d3d12/D3D12_UAV_DIMENSION_UNKNOWN, direct3d12.d3d12_uav_dimension
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
req.typenames: D3D12_UAV_DIMENSION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_UAV_DIMENSION
 - d3d12/D3D12_UAV_DIMENSION
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
 - D3D12_UAV_DIMENSION
---

# D3D12_UAV_DIMENSION enumeration


## -description

Identifies unordered-access view options.

## -enum-fields

### -field D3D12_UAV_DIMENSION_UNKNOWN:0

The view type is unknown.

### -field D3D12_UAV_DIMENSION_BUFFER:1

View the resource as a buffer.

### -field D3D12_UAV_DIMENSION_TEXTURE1D:2

View the resource as a 1D texture.

### -field D3D12_UAV_DIMENSION_TEXTURE1DARRAY:3

View the resource as a 1D texture array.

### -field D3D12_UAV_DIMENSION_TEXTURE2D:4

View the resource as a 2D texture.

### -field D3D12_UAV_DIMENSION_TEXTURE2DARRAY:5

View the resource as a 2D texture array.

### -field D3D12_UAV_DIMENSION_TEXTURE3D:8

View the resource as a 3D texture array.

## -remarks

Specify one of the values in this enumeration in the <b>ViewDimension</b> member of a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_unordered_access_view_desc">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
