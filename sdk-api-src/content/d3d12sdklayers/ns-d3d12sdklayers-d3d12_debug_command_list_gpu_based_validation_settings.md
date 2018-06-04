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

# D3D12_DEBUG_COMMAND_LIST_GPU_BASED_VALIDATION_SETTINGS structure


## -description


<p class="CCE_Message">[Some information relates to pre-released product which may be substantially modified before it's commercially released. Microsoft makes no warranties, express or implied, with respect to the information provided here.]

Describes per-command-list settings used by GPU-Based Validation.  


## -struct-fields




### -field ShaderPatchMode

Specifies a <a href="https://msdn.microsoft.com/A7E7D1E5-8547-4898-B139-EF909D8B5630">D3D12_GPU_BASED_VALIDATION_SHADER_PATCH_MODE</a> that overrides the default device-level shader patch mode (see <a href="https://msdn.microsoft.com/D97086C6-CED8-4C4E-ADA1-7A172B3202F3">ID3D12DebugDevice1::SetDebugParameter</a>).  By default this value is initialized to the <i>DefaultShaderPatchMode</i> assigned to the device (see <a href="https://msdn.microsoft.com/2C4E7A8D-CC42-4C2E-848E-7DA3ECA24391">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a>.


## -remarks





Point to an object using this structure with the <i>pData</i> member of <a href="https://msdn.microsoft.com/8D93895A-BED7-4A86-893B-ACB5FA1B160F">ID3D12DebugCommandList1::SetDebugParameter</a> to configure per-command-list GPU-Based Validation settings.  




## -see-also




<a href="https://msdn.microsoft.com/FE8796A7-98D1-4333-8755-2A47567560B3">Debug Layer Structures</a>



<a href="https://msdn.microsoft.com/0B7ACDC1-D7F6-4565-8E33-F2F14A96E4A8">SetEnableGPUBasedValidation</a>



<a href="https://msdn.microsoft.com/01D1F94F-4DD4-4781-86EF-6C639E8B1069">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

