---
UID: NS:d3d12.D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC
title: D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC
author: windows-sdk-content
description: Describes a raytracing acceleration structure. Pass this structure into ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure to describe the acceleration structure to be built.
old-location: direct3d12\d3d12_build_raytracing_acceleration_structure_desc.htm
tech.root: direct3d12
ms.assetid: C73A3A59-1184-401C-AF45-CBF12419852E
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC, D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC structure, PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC, PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC structure pointer, d3d12/D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC, d3d12/PD3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC, direct3d12.d3d12_build_raytracing_acceleration_structure_desc
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
 - D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC
req.redist: 
---

# D3D12_BUILD_RAYTRACING_ACCELERATION_STRUCTURE_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Describes a raytracing acceleration structure. Pass this structure into <a href="http://docs.microsoft.com/windows/desktop/d3d12/nf-d3d12-id3d12graphicscommandlist4-buildraytracingaccelerationstructure">ID3D12GraphicsCommandList4::BuildRaytracingAccelerationStructure</a> to describe the acceleration structure to be built.


## -struct-fields




### -field DestAccelerationStructureData

Location to store resulting acceleration structure.  <a href="http://docs.microsoft.com/windows/desktop/d3d12/nf-d3d12-id3d12device5-getraytracingaccelerationstructureprebuildinfo">ID3D12Device5::GetRaytracingAccelerationStructurePrebuildInfo</a> reports the amount of memory required for the result here given a set of acceleration structure build parameters.  

The address must be aligned to 256 bytes, defined as <a href="https://docs.microsoft.com/en-us/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BYTE_ALIGNMENT</a>.

The memory pointed to must be in state <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE</a>. 


### -field Inputs

Description of the input data for the acceleration structure build.  This is data is stored in a separate structure because it is also used with <b>GetRaytracingAccelerationStructurePrebuildInfo</b>.


### -field SourceAccelerationStructureData

Address of an existing acceleration structure if an acceleration structure update (an incremental build) is being requested, by setting  <a href="http://docs.microsoft.com/windows/desktop/d3d12/ne-d3d12-d3d12_raytracing_acceleration_structure_build_flags">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BUILD_FLAG_PERFORM_UPDATE</a> in the Flags parameter.  Otherwise this address must be NULL.

If this address is the same as <i>DestAccelerationStructureData</i>, the update is to be performed in-place.  Any other form of overlap of the source and destination memory is invalid and produces undefined behavior.

The address must be aligned to 256 bytes, defined as <a href="https://docs.microsoft.com/en-us/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BYTE_ALIGNMENT</a>, which should automatically be the case because any existing acceleration structure passed in here would have already been required to be placed with such alignment.

The memory pointed to must be in state <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE</a>. 



#### ScratchAccelerationStructureData

Location where the build will store temporary data.  <b>GetRaytracingAccelerationStructurePrebuildInfo</b> reports the amount of scratch memory the implementation will need for a given set of acceleration structure build parameters.  


### -field ScratchAccelerationStructureData

 



