---
UID: NS:d3d12.D3D12_RAYTRACING_INSTANCE_DESC
title: D3D12_RAYTRACING_INSTANCE_DESC
author: windows-sdk-content
description: Describes an instance of a raytracing acceleration structure used in GPU memory during the acceleration structure build process.
old-location: direct3d12\d3d12_raytracing_instance_desc.htm
tech.root: direct3d12
ms.assetid: 816B0281-EC69-4EA1-AE32-6B3E178117DE
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: D3D12_RAYTRACING_INSTANCE_DESC, D3D12_RAYTRACING_INSTANCE_DESC structure, PD3D12_RAYTRACING_INSTANCE_DESC, PD3D12_RAYTRACING_INSTANCE_DESC structure pointer, d3d12/D3D12_RAYTRACING_INSTANCE_DESC, d3d12/PD3D12_RAYTRACING_INSTANCE_DESC, direct3d12.d3d12_raytracing_instance_desc
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
 - D3D12_RAYTRACING_INSTANCE_DESC
product: Windows
targetos: Windows
req.typenames: D3D12_RAYTRACING_INSTANCE_DESC
req.redist: 
---

# D3D12_RAYTRACING_INSTANCE_DESC structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Describes an instance of a raytracing acceleration structure used in GPU memory during the acceleration structure build process.


## -struct-fields




### -field Transform

A 3x4 transform matrix in row-major layout representing the instance-to-world transformation.


### -field InstanceID

  An arbitrary 24-bit value that can be accessed using <b>InstanceID</b> intrinsic function in supported shader types.


### -field InstanceMask

An 8-bit mask assigned to the instance, which can be used to include/reject groups of instances on a per-ray basis. If the value is zero, the instance will never be included, so typically this should be set to some nonzero value. For more information see, the <b>InstanceInclusionMask</b> parameter to the  <b>TraceRay</b> method.


### -field InstanceContributionToHitGroupIndex

Per-instance contribution to add into shader table indexing to select the hit group to use.  


### -field Flags

Flags to apply to the instance.


### -field AccelerationStructure

Address of the bottom-level acceleration structure that is being instanced. The address must be aligned to 256 bytes, defined as <a href="https://docs.microsoft.com/en-us/windows/desktop/direct3d12/constants">D3D12_RAYTRACING_ACCELERATION_STRUCTURE_BYTE_ALIGNMENT</a>. Any existing acceleration structure passed in here would was already been required to be placed with such alignment.

The memory pointed to must be in state <a href="https://msdn.microsoft.com/AB14DE3E-97EA-47BE-8917-805B9651ED3A">D3D12_RESOURCE_STATE_RAYTRACING_ACCELERATION_STRUCTURE</a>. 




## -remarks



This C++ struct definition is useful if generating instance data on the CPU first then uploading to the GPU.  But apps are also free to generate instance descriptions directly into GPU memory from compute shaders for instance, following the same layout.



