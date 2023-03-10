---
UID: NS:d3d12.D3D12_RAYTRACING_SHADER_CONFIG
title: D3D12_RAYTRACING_SHADER_CONFIG (d3d12.h)
description: A state subobject that represents a shader configuration.
helpviewer_keywords: ["D3D12_RAYTRACING_SHADER_CONFIG","D3D12_RAYTRACING_SHADER_CONFIG structure","PD3D12_RAYTRACING_SHADER_CONFIG","PD3D12_RAYTRACING_SHADER_CONFIG structure pointer","d3d12/D3D12_RAYTRACING_SHADER_CONFIG","d3d12/PD3D12_RAYTRACING_SHADER_CONFIG","direct3d12.d3d12_raytracing_shader_config"]
old-location: direct3d12\d3d12_raytracing_shader_config.htm
tech.root: direct3d12
ms.assetid: 8B34EAEF-0B8A-4FE6-81E1-C3652CB5CF6A
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_SHADER_CONFIG, D3D12_RAYTRACING_SHADER_CONFIG structure, PD3D12_RAYTRACING_SHADER_CONFIG, PD3D12_RAYTRACING_SHADER_CONFIG structure pointer, d3d12/D3D12_RAYTRACING_SHADER_CONFIG, d3d12/PD3D12_RAYTRACING_SHADER_CONFIG, direct3d12.d3d12_raytracing_shader_config
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
req.typenames: D3D12_RAYTRACING_SHADER_CONFIG
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_SHADER_CONFIG
 - d3d12/D3D12_RAYTRACING_SHADER_CONFIG
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
 - D3D12_RAYTRACING_SHADER_CONFIG
---

# D3D12_RAYTRACING_SHADER_CONFIG structure


## -description

A state subobject that represents a shader configuration.

## -struct-fields

### -field MaxPayloadSizeInBytes

The maximum storage for scalars (counted as 4 bytes each) in ray payloads in raytracing pipelines that contain this program.

### -field MaxAttributeSizeInBytes

The maximum number of scalars (counted as 4 bytes each) that can be used for attributes in pipelines that contain this shader. The value cannot exceed <a href="/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_MAX_ATTRIBUTE_SIZE_IN_BYTES</a>.

## -remarks

A raytracing pipeline needs one raytracing shader configuration.  If multiple shader configurations are present, such as one in each collection to enable independent driver compilation for each one, they must all match when combined into a raytracing pipeline.