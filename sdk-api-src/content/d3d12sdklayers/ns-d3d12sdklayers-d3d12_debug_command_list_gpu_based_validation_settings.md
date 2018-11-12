---
UID: NS:d3d12sdklayers.D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
title: D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
author: windows-sdk-content
description: Describes per-command-list settings used by GPU-Based Validation.
old-location: direct3d12\d3d12_debug_command_list_gpu_based_validation_settings.htm
tech.root: direct3d12
ms.assetid: CAFEFC8D-9A7A-4DB2-AFEC-69B1ABE87C82
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS, D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS structure, d3d12sdklayers/D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS, direct3d12.d3d12_debug_command_list_gpu_based_validation_settings
ms.prod: windows
ms.technology: windows-sdk
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
 - D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
product: Windows
targetos: Windows
req.typenames: D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS
req.redist: 
---

# D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS structure


## -description


Describes per-command-list settings used by GPU-Based Validation.  


## -struct-fields




### -field ShaderPatchMode

Specifies a <a href="https://msdn.microsoft.com/en-us/library/Mt762984(v=VS.85).aspx">D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE</a> that overrides the default device-level shader patch mode (see <a href="https://msdn.microsoft.com/en-us/library/Mt762994(v=VS.85).aspx">ID3D12DebugDevice1::SetDebugParameter</a>).  By default this value is initialized to the <i>DefaultShaderPatchMode</i> assigned to the device (see <a href="https://msdn.microsoft.com/en-us/library/Mt762981(v=VS.85).aspx">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a>.


## -remarks



Point to an object using this structure with the <i>pData</i> member of <a href="https://msdn.microsoft.com/en-us/library/Mt762989(v=VS.85).aspx">ID3D12DebugCommandList1::SetDebugParameter</a> to configure per-command-list GPU-Based Validation settings.  




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950152(v=VS.85).aspx">Debug Layer Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt762995(v=VS.85).aspx">SetEnableGPUBasedValidation</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt490477(v=VS.85).aspx">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

