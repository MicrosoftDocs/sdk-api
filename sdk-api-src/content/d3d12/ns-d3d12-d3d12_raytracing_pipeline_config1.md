---
UID: NS:d3d12.D3D12_RAYTRACING_PIPELINE_CONFIG1
title: D3D12_RAYTRACING_PIPELINE_CONFIG1
description: A state subobject that represents a raytracing pipeline configuration, with flags.
tech.root: direct3d12
ms.date: 08/05/2021
req.construct-type: structure
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
req.typenames: D3D12_RAYTRACING_PIPELINE_CONFIG1
req.redist: 
f1_keywords:
 - D3D12_RAYTRACING_PIPELINE_CONFIG1
 - d3d12/D3D12_RAYTRACING_PIPELINE_CONFIG1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_RAYTRACING_PIPELINE_CONFIG1
---

## -description

A state subobject that represents a raytracing pipeline configuration, with flags.

**D3D12_RAYTRACING_PIPELINE_CONFIG1** requires Tier 1.1 raytracing support (see [D3D12_RAYTRACING_TIER](/windows/win32/api/d3d12/ne-d3d12-d3d12_raytracing_tier)).

## -struct-fields

### -field MaxTraceRecursionDepth

Type: **[UINT](/windows/win32/winprog/windows-data-types)**

Limit on ray recursion for the raytracing pipeline. It must be in the range of 0 to 31. Below the maximum recursion depth, shader invocations such as closest hit or miss shaders can call **TraceRay** any number of times. At the maximum recursion depth, **TraceRay** calls result in the device going into removed state.

### -field Flags

Type: **[D3D12_RAYTRACING_PIPELINE_FLAGS](./ne-d3d12-d3d12_raytracing_pipeline_flags.md)**

Configuration flags for the raytracing pipeline.

## -remarks

A raytracing pipeline needs one raytracing pipeline configuration. If multiple pipeline configurations are present, then they must all match in content. But there's no benefit to such duplication. For example, defining it once per collection doesn't help drivers do early shader compilation before a raytracing pipeline is created. This is unlike [D3D12_RAYTRACING_SHADER_CONFIG](/windows/win32/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config), which *does* benefit from duplication per collection.

## -see-also
