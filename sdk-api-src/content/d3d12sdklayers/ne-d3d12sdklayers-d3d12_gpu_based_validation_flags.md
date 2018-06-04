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

# D3D12_GPU_BASED_VALIDATION_FLAGS enumeration


## -description


Describes the level of GPU-based validation to perform at runtime.


## -enum-fields




### -field D3D12_GPU_BASED_VALIDATION_FLAGS_NONE

Default behavior; resource states, descriptors, and descriptor tables are all validated.


### -field D3D12_GPU_BASED_VALIDATION_FLAGS_DISABLE_STATE_TRACKING

When set, GPU-based validation does not perform resource state validation which greatly reduces the performance cost of GPU-based validtion. Descriptors and descriptor heaps are still validated.


## -remarks



This enumeration is used with the <a href="https://msdn.microsoft.com/EA774CC4-7675-46AA-9CDF-56C8B9507702">ID3D12Debug2::SetGPUBasedValidationFlags</a> method to configure the amount of runtime validation that will occur.




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

