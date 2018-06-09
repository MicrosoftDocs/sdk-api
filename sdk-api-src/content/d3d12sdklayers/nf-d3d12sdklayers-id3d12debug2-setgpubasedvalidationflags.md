---
UID: NF:d3d12sdklayers.ID3D12Debug2.SetGPUBasedValidationFlags
title: ID3D12Debug2::SetGPUBasedValidationFlags
author: windows-sdk-content
description: This method configures the level of GPU-based validation that the debug device is to perform at runtime.
old-location: direct3d12\id3d12debug2_setgpubasedvalidationflags.htm
old-project: direct3d12
ms.assetid: EA774CC4-7675-46AA-9CDF-56C8B9507702
ms.author: windowssdkdev
ms.date: 06/04/2018
ms.keywords: ID3D12Debug2 interface,SetGPUBasedValidationFlags method, ID3D12Debug2.SetGPUBasedValidationFlags, ID3D12Debug2::SetGPUBasedValidationFlags, SetGPUBasedValidationFlags, SetGPUBasedValidationFlags method, SetGPUBasedValidationFlags method,ID3D12Debug2 interface, d3d12sdklayers/ID3D12Debug2::SetGPUBasedValidationFlags, direct3d12.id3d12debug2_setgpubasedvalidationflags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: D3D12_RLDO_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12sdklayers.h
api_name:
 - ID3D12Debug2.SetGPUBasedValidationFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ID3D12Debug2::SetGPUBasedValidationFlags


## -description


This method configures the level of GPU-based validation that the debug device is to perform at runtime.


## -parameters




### -param Flags

Type: <b><a href="https://msdn.microsoft.com/D9FA7F77-8DE8-4630-A9C7-E95B9E997E23">D3D12_GPU_BASED_VALIDATION_FLAGS</a></b>

Specifies the level of GPU-based validation to perform at runtime.


## -returns



This method does not return a value.




## -remarks



This method overrides the default behavior of GPU-based validation so it must be called before creating the D3D12 Device. These settings can't be changed or cancelled after the device is created. If you want to change the behavior of GPU-based validation at a later time, the device must be destroyed and recreated with different parameters.




## -see-also




<a href="https://msdn.microsoft.com/7FC7A17B-9DD3-4B6C-998E-F958AA1C56FC">ID3D12Debug2</a>
 

 

