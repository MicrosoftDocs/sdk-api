---
UID: NS:d3d12.D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO
title: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO (d3d12.h)
description: Represents prebuild information about a raytracing acceleration structure. Get an instance of this structure by calling GetRaytracingAccelerationStructurePrebuildInfo.
helpviewer_keywords: ["D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO","D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO structure","PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO","PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO structure pointer","d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO","d3d12/PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO","direct3d12.d3d12_raytracing_acceleration_structure_prebuild_info"]
old-location: direct3d12\d3d12_raytracing_acceleration_structure_prebuild_info.htm
tech.root: direct3d12
ms.assetid: B9F9551D-CB2F-488E-AD29-BCE603195F53
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO structure, PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO, PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO structure pointer, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO, d3d12/PD3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO, direct3d12.d3d12_raytracing_acceleration_structure_prebuild_info
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
req.typenames: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO
 - d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO
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
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO
---

# D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO structure


## -description

Represents prebuild information about a raytracing acceleration structure. Get an instance of this structure by calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo">GetRaytracingAccelerationStructurePrebuildInfo</a>.

## -struct-fields

### -field ResultDataMaxSizeInBytes

Size required to hold the result of an acceleration structure build based on the specified inputs.

### -field ScratchDataSizeInBytes

Scratch storage on the GPU required during acceleration structure build based on the specified inputs.



#### UpdateScratchDataSizeInBytes

Scratch storage on GPU required during an acceleration structure update based on the specified inputs.  This only needs to be called for the original acceleration structure build, and defines the scratch storage requirement for every acceleration structure update, other than the initial build.

If the <a href="/windows/desktop/api/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAG_ALLOW_UPDATE</a> flag is not specified when calling <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo">GetRaytracingAccelerationStructurePrebuildInfo</a>, the returned value of this field is 0.

### -field UpdateScratchDataSizeInBytes