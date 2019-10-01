---
UID: NE:d3d12.D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE
title: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE (d3d12.h)
author: windows-sdk-content
description: Specifies the type of acceleration structure post-build info that can be retrieved with calls to EmitRaytracingAccelerationStructurePostbuildInfo and BuildRaytracingAccelerationStructure.
old-location: direct3d12\d3d12_raytracing_acceleration_structure_postbuild_info_type.htm
tech.root: direct3d12
ms.assetid: 91DFA503-7899-4F18-85B3-953F4B9F03A6
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE, D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE enumeration, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION, d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE, direct3d12.d3d12_raytracing_acceleration_structure_postbuild_info_type
ms.topic: enum
f1_keywords: 
 - "d3d12/D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE"
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
 - D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE
targetos: Windows
req.typenames: D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE
req.redist: 
ms.custom: 19H1
---

# D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TYPE enumeration


## -description


Specifies the type of acceleration structure post-build info that can be retrieved with calls to <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-emitraytracingaccelerationstructurepostbuildinfo">EmitRaytracingAccelerationStructurePostbuildInfo</a> and  <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure">BuildRaytracingAccelerationStructure</a>.


## -enum-fields




### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE

The post-build info is space requirements for an acceleration structure after compaction. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_compacted_size_desc">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_COMPACTED_SIZE_DESC</a>.


### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION

The post-build info is space requirements for generating tools visualization for an acceleration structure. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_tools_visualization_desc">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_TOOLS_VISUALIZATION_DESC</a>.


### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION

The post-build info is space requirements for serializing an acceleration structure. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_serialization_desc">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_SERIALIZATION_DESC</a>.


### -field D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE

The post-build info is size of the current acceleration structure. For more information, see <a href="https://docs.microsoft.com/windows/desktop/api/d3d12/ns-d3d12-d3d12_raytracing_acceleration_structure_postbuild_info_current_size_desc">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_POSTBUILD_INFO_CURRENT_SIZE_DESC</a>.

