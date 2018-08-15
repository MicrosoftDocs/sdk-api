---
UID: NE:d3d12sdklayers.D3D12_DEBUG_DEVICE_PARAMETER_TYPE
title: D3D12_DEBUG_DEVICE_PARAMETER_TYPE
author: windows-sdk-content
description: Specifies the data type of the memory pointed to by the pData parameter of ID3D12DebugDevice1::SetDebugParameter and ID3D12DebugDevice1::GetDebugParameter.
old-location: direct3d12\d3d12_debug_device_parameter_type.htm
old-project: direct3d12
ms.assetid: 477155FF-9DF7-4E21-AF52-21EB3DBC3550
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS, D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS, D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR, D3D12_DEBUG_DEVICE_PARAMETER_TYPE, D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_TYPE, direct3d12.d3d12_debug_device_parameter_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: d3d12sdklayers.h
req.include-header: 
req.redist: 
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
req.typenames: D3D12_DEBUG_DEVICE_PARAMETER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12sdklayers.h
api_name:
 - D3D12_DEBUG_DEVICE_PARAMETER_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration


## -description


Specifies the data type of the memory pointed to by the <i>pData</i> parameter of <a href="https://msdn.microsoft.com/D97086C6-CED8-4C4E-ADA1-7A172B3202F3">ID3D12DebugDevice1::SetDebugParameter</a> and <a href="https://msdn.microsoft.com/13A7E7D6-FF00-4E17-A7C5-C383F93F6A06">ID3D12DebugDevice1::GetDebugParameter</a>.


## -enum-fields




### -field D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS

Indicates <i>pData</i> points to a <a href="https://msdn.microsoft.com/36E0A5DC-8313-4D9D-988C-21E6FFCC8730">D3D12_DEBUG_FEATURE</a> value.


### -field D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS

Indicates <i>pData</i> points to a <a href="https://msdn.microsoft.com/2C4E7A8D-CC42-4C2E-848E-7DA3ECA24391">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a> structure.


### -field D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR

Indicates <i>pData</i> points to a <a href="https://msdn.microsoft.com/C137DFAA-7AB9-49A6-882D-61ADE6E9E046">D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/6E76C857-128E-4F0E-9711-72C4CF6C835C">Debug Layer Enumerations</a>



<a href="https://msdn.microsoft.com/01D1F94F-4DD4-4781-86EF-6C639E8B1069">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

