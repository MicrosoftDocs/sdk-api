---
UID: NE:d3d12sdklayers.D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE
title: D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE
author: windows-sdk-content
description: Specifies the type of shader patching used by GPU-Based Validation at either the device or command list level.
old-location: direct3d12\d3d12_gpu_based_validation_shader_patch_mode.htm
old-project: direct3d12
ms.assetid: A7E7D1E5-8547-4898-B139-EF909D8B5630
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE, D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE enumeration, D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_GUARDED_VALIDATION, D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_NONE, D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_STATE_TRACKING_ONLY, D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_UNGUARDED_VALIDATION, NUM_D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODES, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_GUARDED_VALIDATION, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_NONE, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_STATE_TRACKING_ONLY, d3d12sdklayers/D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_UNGUARDED_VALIDATION, d3d12sdklayers/NUM_D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODES, direct3d12.d3d12_gpu_based_validation_shader_patch_mode
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12sdklayers.h
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
req.typenames: D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE enumeration


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Specifies the type of shader patching used by GPU-Based Validation at either the device or command list level.


## -enum-fields




### -field D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_NONE

No shader patching is to be done.  This will retain the original shader bytecode.  Can lead to errors in some of the GPU-Based Validation state tracking as the unpatched shader may still change resource state (see <a href="https://msdn.microsoft.com/library/Dn899226(v=VS.85).aspx">Common state promotion</a>) but the promotion will be untracked without patching the shader.  This can improve performance but no validation will be performed and may also lead to misleading GPU-Based Validation errors. Use this mode very carefully. 


### -field D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_STATE_TRACKING_ONLY

Shaders can be patched with resource state tracking code but no validation.  This may improve performance but no validation will be performed.


### -field D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_UNGUARDED_VALIDATION

The default. Shaders are patched with validation code but erroneous instructions will still be executed.  


### -field D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE_GUARDED_VALIDATION

Shaders are patched with validation code and erroneous instructions are skipped in execution.  This can help avoid crashes or device removal.


### -field NUM_D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODES

Unused, simply the count of the number of modes.


## -remarks



This enum is used by the <a href="https://msdn.microsoft.com/2C4E7A8D-CC42-4C2E-848E-7DA3ECA24391">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>



<a href="https://msdn.microsoft.com/01D1F94F-4DD4-4781-86EF-6C639E8B1069">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

