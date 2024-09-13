---
UID: NF:d3d12.ID3D12Device5.GetRaytracingAccelerationStructurePrebuildInfo
title: ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo (d3d12.h)
description: Query the driver for resource requirements to build an acceleration structure.
helpviewer_keywords: ["GetRaytracingAccelerationStructurePrebuildInfo","GetRaytracingAccelerationStructurePrebuildInfo method","GetRaytracingAccelerationStructurePrebuildInfo method","ID3D12Device5 interface","ID3D12Device5 interface","GetRaytracingAccelerationStructurePrebuildInfo method","ID3D12Device5.GetRaytracingAccelerationStructurePrebuildInfo","ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo","d3d12/ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo","direct3d12.id3d12device5_getraytracingaccelerationstructureprebuildinfo"]
old-location: direct3d12\id3d12device5_getraytracingaccelerationstructureprebuildinfo.htm
tech.root: direct3d12
ms.assetid: 6B2CB3E8-06F8-4578-8FF0-566246C983B0
ms.date: 12/05/2018
ms.keywords: GetRaytracingAccelerationStructurePrebuildInfo, GetRaytracingAccelerationStructurePrebuildInfo method, GetRaytracingAccelerationStructurePrebuildInfo method,ID3D12Device5 interface, ID3D12Device5 interface,GetRaytracingAccelerationStructurePrebuildInfo method, ID3D12Device5.GetRaytracingAccelerationStructurePrebuildInfo, ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo, d3d12/ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo, direct3d12.id3d12device5_getraytracingaccelerationstructureprebuildinfo
req.header: d3d12.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1809 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3d12.lib
req.dll: D3d12.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: RS5, 19H1
f1_keywords:
 - ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo
 - d3d12/ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12.dll
api_name:
 - ID3D12Device5.GetRaytracingAccelerationStructurePrebuildInfo
---

## -description

Query the driver for resource requirements to build an acceleration structure.

## -parameters

### -param pDesc [in]

Description of the acceleration structure build. This structure is shared with <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure">BuildRaytracingAccelerationStructure</a>.  For more information, see <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_build_raytracing_acceleration_structure_inputs">D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_INPUTS</a>.

The implementation is allowed to look at all the CPU parameters in this struct and nested structs.  It may not inspect/dereference any GPU virtual addresses, other than to check to see if a pointer is NULL or not, such as the optional transform in <a href="/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_geometry_triangles_desc">D3D12_RAYTRACING_GEOMETRY_TRIANGLES_DESC</a>, without dereferencing it. In other words, the calculation of resource requirements for the acceleration structure does not depend on the actual geometry data (such as vertex positions), rather it can only depend on overall properties, such as the number of triangles, number of instances etc.

### -param pInfo [out]

The result of the query (in a [D3D12_RAYTRACING_ACCELERATION_STRUCTURE_PREBUILD_INFO](./ns-d3d12-d3d12_raytracing_acceleration_structure_prebuild_info.md) structure).

## -remarks

The input acceleration structure description is the same as what goes into <a href="/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure">BuildRaytracingAccelerationStructure</a>. The result of this function lets the application provide the correct amount of output storage and scratch storage to <b>BuildRaytracingAccelerationStructure</b> given the same geometry.  

Builds can also be done with the same configuration passed to <b>GetAccelerationStructurePrebuildInfo</b> overall except equal or smaller counts for the number of geometries/instances or the  number of vertices/indices/AABBs in any given geometry.  In this case the storage requirements reported with the original sizes passed to <b>GetRaytracingAccelerationStructurePrebuildInfo</b> will be valid – the build may actually consume less space but not more.  This is handy for app scenarios where having conservatively large storage allocated for acceleration structures is fine. 

This method is on the device interface as opposed to command list on the assumption that drivers must be able to calculate resource requirements for an acceleration structure build from only looking at the CPU-visible portions of the call, without having to dereference any pointers to GPU memory containing actual vertex data, index data, etc.

## -see-also

<a href="../d3d12/nn-d3d12-id3d12device5.md">ID3D12Device5</a>
