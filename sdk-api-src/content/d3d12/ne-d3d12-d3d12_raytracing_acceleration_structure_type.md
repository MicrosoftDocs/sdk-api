---
UID: NE:d3d12.D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE
title: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE (d3d12.h)
description: Specifies the type of a raytracing acceleration structure.
helpviewer_keywords: ["D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE enumeration","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_BOTTOM_LEVEL","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_TOP_LEVEL","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_BOTTOM_LEVEL","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_TOP_LEVEL","direct3d12.d3d12_raytracing_acceleration_structure_type"]
old-location: direct3d12\d3d12_raytracing_acceleration_structure_type.htm
tech.root: direct3d12
ms.assetid: 2E77BD31-A04F-4AB3-9C03-E1A7D1C962AD
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE enumeration, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_BOTTOM_LEVEL, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_TOP_LEVEL, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_BOTTOM_LEVEL, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_TOP_LEVEL, direct3d12.d3d12_raytracing_acceleration_structure_type
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
req.typenames: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE
 - d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE
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
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE
---

# D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE enumeration


## -description

Specifies the type of a raytracing acceleration structure.

## -enum-fields

### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_TOP_LEVEL:0

Top-level acceleration structure.

### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_TYPE_BOTTOM_LEVEL:0x1

Bottom-level acceleration structure.

## -remarks

Bottom-level acceleration structures each consist of a set of geometries that are building blocks for a scene. A top-level acceleration structure represents a set of instances of bottom-level acceleration structures.

