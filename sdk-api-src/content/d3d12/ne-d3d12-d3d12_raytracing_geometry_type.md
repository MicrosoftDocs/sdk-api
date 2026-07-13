---
UID: NE:d3d12.D3D12_RAYTRACING_GEOMETRY_TYPE
title: D3D12_RAYTRACING_GEOMETRY_TYPE (d3d12.h)
description: Specifies the type of geometry used for raytracing. Use a value from this enumeration to specify the geometry type in a D3D12_RAYTRACING_GEOMETRY_DESC.
helpviewer_keywords: ["D3D12_RAYTRACING_GEOMETRY_TYPE","D3D12_RAYTRACING_GEOMETRY_TYPE enumeration","D3D12_RAYTRACING_GEOMETRY_TYPE_PROCEDURAL_PRIMITIVE_AABBS","D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES","d3d12/D3D12_RAYTRACING_GEOMETRY_TYPE","d3d12/D3D12_RAYTRACING_GEOMETRY_TYPE_PROCEDURAL_PRIMITIVE_AABBS","d3d12/D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES","direct3d12.d3d12_raytracing_geometry_type"]
old-location: direct3d12\d3d12_raytracing_geometry_type.htm
tech.root: direct3d12
ms.assetid: 97CD5F34-598B-4F3D-851D-C1A62703F6A7
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_GEOMETRY_TYPE, D3D12_RAYTRACING_GEOMETRY_TYPE enumeration, D3D12_RAYTRACING_GEOMETRY_TYPE_PROCEDURAL_PRIMITIVE_AABBS, D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES, d3d12/D3D12_RAYTRACING_GEOMETRY_TYPE, d3d12/D3D12_RAYTRACING_GEOMETRY_TYPE_PROCEDURAL_PRIMITIVE_AABBS, d3d12/D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES, direct3d12.d3d12_raytracing_geometry_type
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
req.typenames: D3D12_RAYTRACING_GEOMETRY_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_GEOMETRY_TYPE
 - d3d12/D3D12_RAYTRACING_GEOMETRY_TYPE
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
 - D3D12_RAYTRACING_GEOMETRY_TYPE
---

# D3D12_RAYTRACING_GEOMETRY_TYPE enumeration


## -description

Specifies the type of geometry used for raytracing. Use a value from this enumeration to specify the geometry type in a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc">D3D12_RAYTRACING_GEOMETRY_DESC</a>.

## -enum-fields

### -field D3D12_RAYTRACING_GEOMETRY_TYPE_TRIANGLES:0

The geometry consists of triangles.

### -field D3D12_RAYTRACING_GEOMETRY_TYPE_PROCEDURAL_PRIMITIVE_AABBS

The geometry procedurally is defined during raytracing by intersection shaders.  For the purpose of acceleration structure builds, the geometry’s bounds are described with axis-aligned bounding boxes using the  <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_aabbs_desc">D3D12_RAYTRACING_GEOMETRY_AABBS_DESC</a> structure.
