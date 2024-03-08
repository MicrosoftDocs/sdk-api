---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS1
title: D3D12_FEATURE_DATA_D3D12_OPTIONS1 (d3d12.h)
description: Describes the level of support for HLSL 6.0 wave operations.
helpviewer_keywords: ["D3D12_FEATURE_DATA_D3D12_OPTIONS1","D3D12_FEATURE_DATA_D3D12_OPTIONS1 structure","d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS1","direct3d12.d3d12_feature_data_d3d12_options1"]
old-location: direct3d12\d3d12_feature_data_d3d12_options1.htm
tech.root: direct3d12
ms.assetid: 39BF7632-AC73-471B-94F9-3128BD0DAB89
ms.date: 12/05/2018
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS1, D3D12_FEATURE_DATA_D3D12_OPTIONS1 structure, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS1, direct3d12.d3d12_feature_data_d3d12_options1
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
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS1
 - d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS1
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
 - D3D12_FEATURE_DATA_D3D12_OPTIONS1
---

# D3D12_FEATURE_DATA_D3D12_OPTIONS1 structure


## -description

Describes the level of support for HLSL 6.0 wave operations.

## -struct-fields

### -field WaveOps

True if the driver supports HLSL 6.0 wave operations.

### -field WaveLaneCountMin

Specifies the baseline number of lanes in the SIMD wave that this implementation can support. This term is sometimes known as "wavefront size" or "warp width". Currently apps should rely only on this minimum value for sizing workloads.

### -field WaveLaneCountMax

Specifies the maximum number of lanes in the SIMD wave that this implementation can support.

### -field TotalLaneCount

Specifies the total number of SIMD lanes on the hardware.

### -field ExpandedComputeResourceStates

Indicates transitions are possible  in and out of the CBV, and indirect argument states, on compute command lists. If <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device-checkfeaturesupport">CheckFeatureSupport</a> succeeds this value will always be true.

### -field Int64ShaderOps

Indicates that 64bit integer operations are supported.

## -remarks

A "lane" is  single thread of execution. The shader models before version 6.0 expose only one of these at the language level, leaving expansion to parallel SIMD processing entirely up to the implementation. 

 

A "wave" is  set of lanes (threads) executed simultaneously in the processor. No explicit barriers are required to guarantee that they execute in parallel. Similar concepts include "warp" and "wavefront". 


This structure is used with the D3D12_FEATURE_D3D12_OPTIONS1 member of  <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-structures">Core Structures</a>



<a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_feature">D3D12_FEATURE</a>
