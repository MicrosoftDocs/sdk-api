---
UID: NF:d3d12.ID3D12GraphicsCommandList4.EmitRaytracingAccelerationStructurePostbuildInfo
title: ID3D12GraphicsCommandList4::EmitRaytracingAccelerationStructurePostbuildInfo
author: windows-sdk-content
description: Emits post-build properties for a set of acceleration structures. This enables applications to know the output resource requirements for performing acceleration structure operations via ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure.
old-location: direct3d12\id3d12graphicscommandlist4_emitraytracingaccelerationstructurepostbuildinfo.htm
tech.root: direct3d12
ms.assetid: 05E4B38B-1A3A-4121-8BD7-A437534C8B9A
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: EmitRaytracingAccelerationStructurePostbuildInfo, EmitRaytracingAccelerationStructurePostbuildInfo method, EmitRaytracingAccelerationStructurePostbuildInfo method,ID3D12GraphicsCommandList4 interface, ID3D12GraphicsCommandList4 interface,EmitRaytracingAccelerationStructurePostbuildInfo method, ID3D12GraphicsCommandList4.EmitRaytracingAccelerationStructurePostbuildInfo, ID3D12GraphicsCommandList4::EmitRaytracingAccelerationStructurePostbuildInfo, d3d12/ID3D12GraphicsCommandList4::EmitRaytracingAccelerationStructurePostbuildInfo, direct3d12.id3d12graphicscommandlist4_emitraytracingaccelerationstructurepostbuildinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.lib: D3D12.lib
req.dll: D3D12.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D12.dll
api_name:
 - ID3D12GraphicsCommandList4.EmitRaytracingAccelerationStructurePostbuildInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID3D12GraphicsCommandList4::EmitRaytracingAccelerationStructurePostbuildInfo


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Emits post-build properties for a set of acceleration structures.  This enables applications to know the output resource requirements for performing acceleration structure operations via <a href="http://docs.microsoft.com/windows/desktop/d3d12/nf-d3d12-id3d12graphicscommandlist4-copyraytracingaccelerationstructure">ID3D12GraphicsCommandList4::CopyRaytracingAccelerationStructure</a>.


## -parameters




### -param pDesc [in]

Description of pos-tbuild information to generate.


### -param NumSourceAccelerationStructures [in]

Number of pointers to acceleration structure GPU virtual addresses pointed to by <i>pSourceAccelerationStructureData</i>.  This number also affects the destination (output), which will be a contiguous array of <b>NumSourceAccelerationStructures</b> output structures, where the type of the structures depends on <i>InfoType</i> field of the supplied in the <i>pDesc</i> description.  


### -param pSourceAccelerationStructureData [in]

Pointer to array of GPU virtual addresses of size <i>NumSourceAccelerationStructures</i>.

The address must be aligned to 256 bytes, defined as <a href="https://docs.microsoft.com/en-us/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BYTE_ALIGNMENT</a>. 

The memory pointed to must be in state <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE</a>. 


## -returns



This method does not return a value.




## -remarks



This method can be called from graphics or compute command lists but not from bundles.




## -see-also




<a href="direct3d12.id3d12graphicscommandlist4">ID3D12GraphicsCommandList4</a>
 

 

