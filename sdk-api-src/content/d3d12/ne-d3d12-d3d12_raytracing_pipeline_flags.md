---
UID: NE:d3d12.D3D12_RAYTRACING_PIPELINE_FLAGS
title: D3D12_RAYTRACING_PIPELINE_FLAGS
description: Defines constants that specify configuration flags for a raytracing pipeline.
tech.root: direct3d12
ms.date: 08/05/2021
req.construct-type: enumeration
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
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
req.redist: 
f1_keywords:
 - D3D12_RAYTRACING_PIPELINE_FLAGS
 - d3d12/D3D12_RAYTRACING_PIPELINE_FLAGS
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RAYTRACING_PIPELINE_FLAGS
---

## -description

Defines constants that specify configuration flags for a raytracing pipeline.

## -enum-fields

### -field D3D12_RAYTRACING_PIPELINE_FLAG_NONE:0

Specifies no option.

### -field D3D12_RAYTRACING_PIPELINE_FLAG_SKIP_TRIANGLES:0x100

Specifies that for any **TraceRay** call within this raytracing pipeline, the [RAY_FLAG_SKIP_TRIANGLES](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags) ray flag should be added in. The resulting combination of ray flags must be valid. The presence of this flag in a raytracing pipeline config doesn't show up in a **RayFlags** call from a shader. Implementations might be able to optimize pipelines knowing that a particular primitive type need not be considered.

### -field D3D12_RAYTRACING_PIPELINE_FLAG_SKIP_PROCEDURAL_PRIMITIVES:0x200

Specifies that for any **TraceRay** call within this raytracing pipeline, the [RAY_FLAG_SKIP_PROCEDURAL_PRIMITIVES](/windows/win32/api/d3d12/ne-d3d12-d3d12_ray_flags) ray flag should be added in.

## -remarks

## -see-also
