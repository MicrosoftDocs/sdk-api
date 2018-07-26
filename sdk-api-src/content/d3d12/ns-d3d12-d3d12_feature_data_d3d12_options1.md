---
UID: NS:d3d12.D3D12_FEATURE_DATA_D3D12_OPTIONS1
title: D3D12_FEATURE_DATA_D3D12_OPTIONS1
author: windows-sdk-content
description: Describes the level of support for HLSL 6.0 wave operations.
old-location: direct3d12\d3d12_feature_data_d3d12_options1.htm
old-project: direct3d12
ms.assetid: 39BF7632-AC73-471B-94F9-3128BD0DAB89
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: D3D12_FEATURE_DATA_D3D12_OPTIONS1, D3D12_FEATURE_DATA_D3D12_OPTIONS1 structure, d3d12/D3D12_FEATURE_DATA_D3D12_OPTIONS1, direct3d12.d3d12_feature_data_d3d12_options1
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: D3D12_FEATURE_DATA_D3D12_OPTIONS1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12.h
api_name:
 - D3D12_FEATURE_DATA_D3D12_OPTIONS1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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

Specifies the maximum number of lanes in the SIMD wave that this implementation can support. This capability is reserved for future expansion, and is not expected to be used by current applications. 



### -field TotalLaneCount

Specifies the total number of SIMD lanes on the hardware.


### -field ExpandedComputeResourceStates

Indicates transitions are possible  in and out of the CBV, and indirect argument states, on compute command lists. If <a href="https://msdn.microsoft.com/2E986E37-30C7-45FE-BC8B-A6DD5670938F">CheckFeatureSupport</a> succeeds this value will always be true. 


### -field Int64ShaderOps

Indicates that 64bit integer operations are supported.


## -remarks



A "lane" is  single thread of execution. The shader models before version 6.0 expose only one of these at the language level, leaving expansion to parallel SIMD processing entirely up to the implementation. 

 

A "wave" is  set of lanes (threads) executed simultaneously in the processor. No explicit barriers are required to guarantee that they execute in parallel. Similar concepts include "warp" and "wavefront". 


This structure is used with the D3D12_FEATURE_D3D12_OPTIONS1 member of  <a href="https://msdn.microsoft.com/165ECFE0-1B18-4A26-8B9C-3CE53776A349">D3D12_FEATURE</a>.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

