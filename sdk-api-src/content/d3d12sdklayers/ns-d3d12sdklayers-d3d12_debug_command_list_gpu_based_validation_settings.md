---
UID: NS:d3d12sdklayers.D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
title: D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS (d3d12sdklayers.h)
description: Describes per-command-list settings used by GPU-Based Validation.
helpviewer_keywords: ["D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS","D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS structure","d3d12sdklayers/D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS","direct3d12.d3d12_debug_command_list_gpu_based_validation_settings"]
old-location: direct3d12\d3d12_debug_command_list_gpu_based_validation_settings.htm
tech.root: direct3d12
ms.assetid: CAFEFC8D-9A7A-4DB2-AFEC-69B1ABE87C82
ms.date: 12/05/2018
ms.keywords: D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS, D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS structure, d3d12sdklayers/D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS, direct3d12.d3d12_debug_command_list_gpu_based_validation_settings
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
targetos: Windows
req.typenames: D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
 - d3d12sdklayers/D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
---

# D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS structure


## -description

Describes per-command-list settings used by GPU-Based Validation.

## -struct-fields

### -field ShaderPatchMode

Specifies a <a href="/windows/desktop/api/d3d12sdklayers/ne-d3d12sdklayers-d3d12_gpu_based_validation_shader_patch_mode">D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE</a> that overrides the default device-level shader patch mode (see <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugdevice1-setdebugparameter">ID3D12DebugDevice1::SetDebugParameter</a>).  By default this value is initialized to the <i>DefaultShaderPatchMode</i> assigned to the device (see <a href="/windows/desktop/api/d3d12sdklayers/ns-d3d12sdklayers-d3d12_debug_device_gpu_based_validation_settings">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a>.

## -remarks

Point to an object using this structure with the <i>pData</i> member of <a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debugcommandlist1-setdebugparameter">ID3D12DebugCommandList1::SetDebugParameter</a> to configure per-command-list GPU-Based Validation settings.

## -see-also

<a href="/windows/desktop/direct3d12/direct3d-12-sdklayers-structures">Debug Layer Structures</a>



<a href="/windows/desktop/api/d3d12sdklayers/nf-d3d12sdklayers-id3d12debug1-setenablegpubasedvalidation">SetEnableGPUBasedValidation</a>



<a href="/windows/desktop/direct3d12/using-d3d12-debug-layer-gpu-based-validation">Using D3D12 Debug Layer GPU-Based Validation</a>