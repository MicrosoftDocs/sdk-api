---
UID: NS:d3d12.D3D12_RAYTRACING_PIPELINE_CONFIG
title: D3D12_RAYTRACING_PIPELINE_CONFIG
author: windows-sdk-content
description: A state subobject that represents a raytracing pipeline configuration.
old-location: direct3d12\d3d12_raytracing_pipeline_config.htm
tech.root: direct3d12
ms.assetid: 4E2A9C75-CCFE-4AB5-967A-FF2CE3C8A7CF
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D3D12_RAYTRACING_PIPELINE_CONFIG, D3D12_RAYTRACING_PIPELINE_CONFIG structure, PD3D12_RAYTRACING_PIPELINE_CONFIG, PD3D12_RAYTRACING_PIPELINE_CONFIG structure pointer, d3d12/D3D12_RAYTRACING_PIPELINE_CONFIG, d3d12/PD3D12_RAYTRACING_PIPELINE_CONFIG, direct3d12.d3d12_raytracing_pipeline_config
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D12.h
api_name:
 - D3D12_RAYTRACING_PIPELINE_CONFIG
product: Windows
targetos: Windows
req.typenames: D3D12_RAYTRACING_PIPELINE_CONFIG
req.redist: 
---

# D3D12_RAYTRACING_PIPELINE_CONFIG structure


## -description


A state subobject that represents a raytracing pipeline configuration.


## -struct-fields




### -field MaxTraceRecursionDepth

Limit on ray recursion for the raytracing pipeline. It must be in the range of 0 to 31. Below the maximum recursion depth, shader invocations such as closest hit or miss shaders can call <b>TraceRay</b> any number of times.  At the maximum recursion depth, <b>TraceRay</b> calls result in the device going into removed state.  


## -remarks



A raytracing pipeline needs one raytracing pipeline configuration.  If multiple pipeline configurations are present they must all match in content.  There is no benefit to such duplication.  For example defining it once per collection doesn’t help drivers do early shader compilation before a raytracing pipeline is created.  This is unlike <a href="http://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_shader_config">D3D12_RAYTRACING_SHADER_CONFIG</a> which does benefit from duplication per collection.



