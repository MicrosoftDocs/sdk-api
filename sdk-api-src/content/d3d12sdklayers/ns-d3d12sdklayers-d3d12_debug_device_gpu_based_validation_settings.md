---
UID: NS:d3d12sdklayers.D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS
title: D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS
author: windows-sdk-content
description: Describes settings used by GPU-Based Validation.
old-location: direct3d12\d3d12_debug_device_gpu_based_validation_settings.htm
tech.root: direct3d12
ms.assetid: 2C4E7A8D-CC42-4C2E-848E-7DA3ECA24391
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS, D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS structure, d3d12sdklayers/D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS, direct3d12.d3d12_debug_device_gpu_based_validation_settings
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: d3d12sdklayers.h
req.include-header: D3d12sdklayers_RS1.h
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
 - d3d12sdklayers.h
api_name:
 - D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS
product: Windows
targetos: Windows
req.typenames: D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS
req.redist: 
---

# D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS structure


## -description


Describes settings used by GPU-Based Validation.  


## -struct-fields




### -field MaxMessagesPerCommandList

Specifies a UINT that limits the number of messages that can be stored in the GPU-Based Validation message log.  The default value is 256.  Since many identical errors can be produced in a single Draw/Dispatch call it may be useful to increase this number.  Note this can become a memory burden if a large number of command lists are used as there is a committed message log per command list.


### -field DefaultShaderPatchMode

Specifies the <a href="https://msdn.microsoft.com/en-us/library/Mt762984(v=VS.85).aspx">D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE</a> that GPU-Based Validation uses when injecting validation code into shaders, except when overridden by per-command-list GPU-Based Validation settings (see <a href="https://msdn.microsoft.com/en-us/library/Mt762979(v=VS.85).aspx">D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS</a>).  The default value is D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_UNGUARDED_VALIDATION.


### -field PipelineStateCreateFlags

Specifies one of the <a href="https://msdn.microsoft.com/en-us/library/Mt762983(v=VS.85).aspx">D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAGS</a> that indicates how GPU-Based Validation handles patching pipeline states.  The default value is D3D12_GPU_BASED_VALIDATION_PIPELINE_STATE_CREATE_FLAG_NONE.


## -remarks



Point to an object using this structure with the <i>pData</i> member of <a href="https://msdn.microsoft.com/en-us/library/Mt762994(v=VS.85).aspx">ID3D12DebugDevice1::SetDebugParameter</a> to configure device-wide GPU-Based Validation settings.  

Individual command lists can override the default shader patch mode using <a href="https://msdn.microsoft.com/en-us/library/Mt762989(v=VS.85).aspx">ID3D12DebugCommandList1::SetDebugParameter</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950152(v=VS.85).aspx">Debug Layer Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt762995(v=VS.85).aspx">SetEnableGPUBasedValidation</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt490477(v=VS.85).aspx">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

