---
UID: NE:d3d12sdklayers.D3D12_DEBUG_DEVICE_PARAMETER_TYPE
title: D3D12_DEBUG_DEVICE_PARAMETER_TYPE
author: windows-sdk-content
description: Specifies the data type of the memory pointed to by the pData parameter of ID3D12DebugDevice1::SetDebugParameter and ID3D12DebugDevice1::GetDebugParameter.
old-location: direct3d12\d3d12_debug_device_parameter_type.htm
tech.root: direct3d12
ms.assetid: 477155FF-9DF7-4E21-AF52-21EB3DBC3550
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS, D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS, D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR, D3D12_DEBUG_DEVICE_PARAMETER_TYPE, D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR, d3d12sdklayers/D3D12_DEBUG_DEVICE_PARAMETER_TYPE, direct3d12.d3d12_debug_device_parameter_type
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
 - D3D12_DEBUG_DEVICE_PARAMETER_TYPE
product: Windows
targetos: Windows
req.typenames: D3D12_DEBUG_DEVICE_PARAMETER_TYPE
req.redist: 
---

# D3D12_DEBUG_DEVICE_PARAMETER_TYPE enumeration


## -description


Specifies the data type of the memory pointed to by the <i>pData</i> parameter of <a href="https://msdn.microsoft.com/en-us/library/Mt762994(v=VS.85).aspx">ID3D12DebugDevice1::SetDebugParameter</a> and <a href="https://msdn.microsoft.com/en-us/library/Mt762992(v=VS.85).aspx">ID3D12DebugDevice1::GetDebugParameter</a>.


## -enum-fields




### -field D3D12_DEBUG_DEVICE_PARAMETER_FEATURE_FLAGS

Indicates <i>pData</i> points to a <a href="https://msdn.microsoft.com/en-us/library/Dn950141(v=VS.85).aspx">D3D12_DEBUG_FEATURE</a> value.


### -field D3D12_DEBUG_DEVICE_PARAMETER_GPU_BASED_VALIDATION_SETTINGS

Indicates <i>pData</i> points to a <a href="https://msdn.microsoft.com/en-us/library/Mt762981(v=VS.85).aspx">D3D12_DEBUG_DEVICE_GPU_BASED_VALIDATION_SETTINGS</a> structure.


### -field D3D12_DEBUG_DEVICE_PARAMETER_GPU_SLOWDOWN_PERFORMANCE_FACTOR

Indicates <i>pData</i> points to a <a href="https://msdn.microsoft.com/en-us/library/Mt492554(v=VS.85).aspx">D3D12_DEBUG_DEVICE_GPU_SLOWDOWN_PERFORMANCE_FACTOR</a> structure.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dn950149(v=VS.85).aspx">Debug Layer Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Mt490477(v=VS.85).aspx">Using D3D12 Debug Layer GPU-Based Validation</a>
 

 

