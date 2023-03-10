---
UID: NE:d3d12.D3D12_RAYTRACING_GEOMETRY_FLAGS
title: D3D12_RAYTRACING_GEOMETRY_FLAGS (d3d12.h)
description: Specifies flags for raytracing geometry in a D3D12_RAYTRACING_GEOMETRY_DESC structure.
helpviewer_keywords: ["D3D12_RAYTRACING_GEOMETRY_FLAGS","D3D12_RAYTRACING_GEOMETRY_FLAGS enumeration","D3D12_RAYTRACING_GEOMETRY_FLAG_NONE","D3D12_RAYTRACING_GEOMETRY_FLAG_NO_DUPLICATE_ANYHIT_INVOCATION","D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE","d3d12/D3D12_RAYTRACING_GEOMETRY_FLAGS","d3d12/D3D12_RAYTRACING_GEOMETRY_FLAG_NONE","d3d12/D3D12_RAYTRACING_GEOMETRY_FLAG_NO_DUPLICATE_ANYHIT_INVOCATION","d3d12/D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE","direct3d12.d3d12_raytracing_geometry_flags"]
old-location: direct3d12\d3d12_raytracing_geometry_flags.htm
tech.root: direct3d12
ms.assetid: E8C7003D-0170-41C4-9124-AF4600A8A7C2
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_GEOMETRY_FLAGS, D3D12_RAYTRACING_GEOMETRY_FLAGS enumeration, D3D12_RAYTRACING_GEOMETRY_FLAG_NONE, D3D12_RAYTRACING_GEOMETRY_FLAG_NO_DUPLICATE_ANYHIT_INVOCATION, D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE, d3d12/D3D12_RAYTRACING_GEOMETRY_FLAGS, d3d12/D3D12_RAYTRACING_GEOMETRY_FLAG_NONE, d3d12/D3D12_RAYTRACING_GEOMETRY_FLAG_NO_DUPLICATE_ANYHIT_INVOCATION, d3d12/D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE, direct3d12.d3d12_raytracing_geometry_flags
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
req.typenames: D3D12_RAYTRACING_GEOMETRY_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_GEOMETRY_FLAGS
 - d3d12/D3D12_RAYTRACING_GEOMETRY_FLAGS
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
 - D3D12_RAYTRACING_GEOMETRY_FLAGS
---

# D3D12_RAYTRACING_GEOMETRY_FLAGS enumeration


## -description

Specifies flags for raytracing geometry in a <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_desc">D3D12_RAYTRACING_GEOMETRY_DESC</a> structure.

## -enum-fields

### -field D3D12_RAYTRACING_GEOMETRY_FLAG_NONE:0

No options specified.

### -field D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE:0x1

When rays encounter this geometry, the geometry acts as if no any hit shader is present.  It is recommended that apps use this flag liberally, as it can enable important ray-processing optimizations.  Note that this behavior can be overridden on a per-instance basis with <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_instance_flags">D3D12_RAYTRACING_INSTANCE_FLAGS</a> and on a per-ray basis using ray flags in <b>TraceRay</b>.

### -field D3D12_RAYTRACING_GEOMETRY_FLAG_NO_DUPLICATE_ANYHIT_INVOCATION:0x2

By default, the system is free to trigger an any hit shader more than once for a given ray-primitive intersection. This flexibility helps improve the traversal efficiency of acceleration structures in certain cases.  For instance, if the acceleration structure is implemented internally with bounding volumes, the implementation may find it beneficial to store relatively long triangles in multiple bounding boxes rather than a larger single box. However, some application use cases require that intersections be reported to the any hit shader at most once. This flag enables that guarantee for the given geometry, potentially with some performance impact.

This flag applies to all geometry types.
