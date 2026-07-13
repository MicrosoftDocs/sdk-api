---
UID: NE:d3d12.D3D12_RAYTRACING_INSTANCE_FLAGS
title: D3D12_RAYTRACING_INSTANCE_FLAGS (d3d12.h)
description: Flags for a raytracing acceleration structure instance. These flags can be used to override D3D12_RAYTRACING_GEOMETRY_FLAGS for individual instances.
helpviewer_keywords: ["D3D12_RAYTRACING_INSTANCE_FLAGS","D3D12_RAYTRACING_INSTANCE_FLAGS enumeration","D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_NON_OPAQUE","D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_OPAQUE","D3D12_RAYTRACING_INSTANCE_FLAG_NONE","D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_CULL_DISABLE","D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_FRONT_COUNTERCLOCKWISE","d3d12/D3D12_RAYTRACING_INSTANCE_FLAGS","d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_NON_OPAQUE","d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_OPAQUE","d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_NONE","d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_CULL_DISABLE","d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_FRONT_COUNTERCLOCKWISE","direct3d12.d3d12_raytracing_instance_flags"]
old-location: direct3d12\d3d12_raytracing_instance_flags.htm
tech.root: direct3d12
ms.assetid: 418D1EF1-FC41-4BEF-914E-A9C82E78567A
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_INSTANCE_FLAGS, D3D12_RAYTRACING_INSTANCE_FLAGS enumeration, D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_NON_OPAQUE, D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_OPAQUE, D3D12_RAYTRACING_INSTANCE_FLAG_NONE, D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_CULL_DISABLE, D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_FRONT_COUNTERCLOCKWISE, d3d12/D3D12_RAYTRACING_INSTANCE_FLAGS, d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_NON_OPAQUE, d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_OPAQUE, d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_NONE, d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_CULL_DISABLE, d3d12/D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_FRONT_COUNTERCLOCKWISE, direct3d12.d3d12_raytracing_instance_flags
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
req.typenames: D3D12_RAYTRACING_INSTANCE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_INSTANCE_FLAGS
 - d3d12/D3D12_RAYTRACING_INSTANCE_FLAGS
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
 - D3D12_RAYTRACING_INSTANCE_FLAGS
---

# D3D12_RAYTRACING_INSTANCE_FLAGS enumeration


## -description

Flags for a raytracing acceleration structure instance. These flags can be used to override <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags">D3D12_RAYTRACING_GEOMETRY_FLAGS</a> for individual instances.

## -enum-fields

### -field D3D12_RAYTRACING_INSTANCE_FLAG_NONE:0

No options specified.

### -field D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_CULL_DISABLE:0x1

Disables front/back face culling for this instance.  The Ray flags <b>RAY_FLAG_CULL_BACK_FACING_TRIANGLES</b> and <b>RAY_FLAG_CULL_FRONT_FACING_TRIANGLES</b> will have no effect on this instance.

### -field D3D12_RAYTRACING_INSTANCE_FLAG_TRIANGLE_FRONT_COUNTERCLOCKWISE:0x2

This flag reverses front and back facings, which is useful if the application’s natural winding order differs from the default. By default, a triangle is front facing if its vertices appear clockwise from the ray origin and back facing if its vertices appear counter-clockwise from the ray origin, in object space in a left-handed coordinate system.  

Since these winding direction rules are defined in object space, they are unaffected by instance transforms.  For example, an instance transform matrix with negative determinant (e.g. mirroring some geometry) does not change the facing of the triangles within the instance.  Per-geometry transforms defined in <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc">D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC</a> ,  by contrast,  get combined with the associated vertex data in object space, so a negative determinant matrix there does flip triangle winding.

### -field D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_OPAQUE:0x4

The instance will act as if   <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags">D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE</a> had been specified for all the geometries in the bottom-level acceleration structure referenced by the instance.  Note that this behavior can be overridden by the ray flag <b>RAY_FLAG_FORCE_NON_OPAQUE</b>.

This flag is mutually exclusive to the <b>D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_NON_OPAQUE</b> flag.

### -field D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_NON_OPAQUE:0x8

The instance will act as if <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_geometry_flags">D3D12_RAYTRACING_GEOMETRY_FLAG_OPAQUE</a> had not been specified for any of the geometries in the bottom-level acceleration structure referenced by the instance. Note that this behavior can be overridden by the ray flag <b>RAY_FLAG_FORCE_OPAQUE</b>.

This flag is mutually exclusive to the <b>D3D12_RAYTRACING_INSTANCE_FLAG_FORCE_OPAQUE</b> flag.
