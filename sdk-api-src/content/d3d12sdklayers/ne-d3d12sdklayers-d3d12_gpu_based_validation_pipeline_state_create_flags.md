---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Specifies how GPU-Based Validation handles patched pipeline states during <a href="https://msdn.microsoft.com/E35FCC4A-7527-4A6C-8569-0801A06AA427">ID3D12Device::CreateGraphicsPipelineState</a> and <a href="https://msdn.microsoft.com/FFA361B2-D8FA-4F5A-8D0C-022C2AA76B57">ID3D12Device::CreateComputePipelineState</a>.


## -enum-fields




### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_NONE

This is the default value.  Indicates no patching of pipeline states should be done during PSO creation.  Instead PSO’s are patched on first use in a command list.  This can help to reduce the up-front cost of PSO creation but may instead slow down command list recording until a steady-state is reached.


### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_TRACKING_ONLY_SHADERS

Indicates that state-tracking GPU-Based Validation PSO’s should be created along with the original PSO at create time.


### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_UNGUARDED_VALIDATION_SHADERS

Indicates that unguarded GPU-Based Validation PSO’s should be created along with the original PSO at create time.


### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_FRONT_LOAD_CREATE_GUARDED_VALIDATION_SHADERS

Indicates that guarded GPU-Based Validation PSO’s should be created along with the original PSO at create time.


### -field D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS_VALID_MASK

Internal use only.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/2C4E7A8D-CC42-4C2E-848E-7DA3ECA24391">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a> structure.

Generally speaking most application developers are likely to leave this parameter unchanged.  However, if the overhead of deferring patched PSO creation is suspected to be too much of a performance problem, then developers should consider changing this setting.




## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>



<a href="https://msdn.microsoft.com/01D1F94F-4DD4-4781-86EF-6C639E8B1069">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

