---
UID: NE:d3d12.D3D12_TEXTURE_COPY_TYPE
title: D3D12_TEXTURE_COPY_TYPE (d3d12.h)
description: Specifies what type of texture copy is to take place.
helpviewer_keywords: ["D3D12_TEXTURE_COPY_TYPE","D3D12_TEXTURE_COPY_TYPE enumeration","D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT","D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX","d3d12/D3D12_TEXTURE_COPY_TYPE","d3d12/D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT","d3d12/D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX","direct3d12.d3d12_texture_copy_type"]
old-location: direct3d12\d3d12_texture_copy_type.htm
tech.root: direct3d12
ms.assetid: CF296200-55A7-46B2-BF2C-58806A6A3BBC
ms.date: 12/05/2018
ms.keywords: D3D12_TEXTURE_COPY_TYPE, D3D12_TEXTURE_COPY_TYPE enumeration, D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT, D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX, d3d12/D3D12_TEXTURE_COPY_TYPE, d3d12/D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT, d3d12/D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX, direct3d12.d3d12_texture_copy_type
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
req.typenames: D3D12_TEXTURE_COPY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_TEXTURE_COPY_TYPE
 - d3d12/D3D12_TEXTURE_COPY_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_TEXTURE_COPY_TYPE
---

# D3D12_TEXTURE_COPY_TYPE enumeration


## -description

Specifies what type of texture copy is to take place.

## -enum-fields

### -field D3D12_TEXTURE_COPY_TYPE_SUBRESOURCE_INDEX:0

Indicates a subresource, identified by an index, is to be copied.

### -field D3D12_TEXTURE_COPY_TYPE_PLACED_FOOTPRINT:1

Indicates a place footprint, identified by a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_placed_subresource_footprint">D3D12_PLACED_SUBRESOURCE_FOOTPRINT</a> structure, is to be copied.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_texture_copy_location">D3D12_TEXTURE_COPY_LOCATION</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
