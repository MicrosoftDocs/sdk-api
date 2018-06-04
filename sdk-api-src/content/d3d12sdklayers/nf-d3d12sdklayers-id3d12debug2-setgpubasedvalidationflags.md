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
 

 

