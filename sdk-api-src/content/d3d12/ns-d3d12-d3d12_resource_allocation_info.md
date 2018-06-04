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

# D3D12_RESOURCE_ALLOCATION_INFO structure


## -description


Describes parameters needed to allocate resources.


## -struct-fields




### -field SizeInBytes

The size, in bytes, of the resource.


### -field Alignment

The alignment value for the resource; one of 4KB (4096), 64KB (65536) and 4MB (4194304) alignment.


## -remarks




        This structure is used by the <a href="https://msdn.microsoft.com/43467E09-835B-4DB9-B0A4-F75868DE4609">GetResourceAllocationInfo</a> method.
      




## -see-also




<a href="https://msdn.microsoft.com/81FC8D0E-2C15-42D3-9E06-1FE193F707C6">CD3DX12_RESOURCE_ALLOCATION_INFO</a>



<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

