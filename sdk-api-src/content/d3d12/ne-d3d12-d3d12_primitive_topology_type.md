---
UID: NE:d3d12.D3D12_PRIMITIVE_TOPOLOGY_TYPE
title: D3D12_PRIMITIVE_TOPOLOGY_TYPE (d3d12.h)
description: Specifies how the pipeline interprets geometry or hull shader input primitives.
helpviewer_keywords: ["D3D12_PRIMITIVE_TOPOLOGY_TYPE","D3D12_PRIMITIVE_TOPOLOGY_TYPE enumeration","D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE","D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH","D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT","D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE","D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED","d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE","d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE","d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH","d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT","d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE","d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED","direct3d12.d3d12_primitive_topology_type"]
old-location: direct3d12\d3d12_primitive_topology_type.htm
tech.root: direct3d12
ms.assetid: 3BD4DF5E-EA91-4B2A-AADE-B9AE0E766F63
ms.date: 12/05/2018
ms.keywords: D3D12_PRIMITIVE_TOPOLOGY_TYPE, D3D12_PRIMITIVE_TOPOLOGY_TYPE enumeration, D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE, D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH, D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT, D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE, D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE, d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED, direct3d12.d3d12_primitive_topology_type
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
req.typenames: D3D12_PRIMITIVE_TOPOLOGY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_PRIMITIVE_TOPOLOGY_TYPE
 - d3d12/D3D12_PRIMITIVE_TOPOLOGY_TYPE
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
 - D3D12_PRIMITIVE_TOPOLOGY_TYPE
---

# D3D12_PRIMITIVE_TOPOLOGY_TYPE enumeration


## -description

Specifies how the pipeline interprets geometry or hull shader input primitives.

## -enum-fields

### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_UNDEFINED:0

The shader has not been initialized with an input primitive type.

### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_POINT:1

Interpret the input primitive as a point.

### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_LINE:2

Interpret the input primitive as a line.

### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_TRIANGLE:3

Interpret the input primitive as a triangle.

### -field D3D12_PRIMITIVE_TOPOLOGY_TYPE_PATCH:4

Interpret the input primitive as a control point patch.

## -remarks

This enum is used by the <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_graphics_pipeline_state_desc">D3D12_GRAPHICS_PIPELINE_STATE_DESC</a> structure.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-enumerations">Core Enumerations</a>
