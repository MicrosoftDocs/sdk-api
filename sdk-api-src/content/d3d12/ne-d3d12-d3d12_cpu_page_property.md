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

# D3D12_CPU_PAGE_PROPERTY enumeration


## -description


Specifies the CPU-page properties for the heap.


## -enum-fields




### -field D3D12_CPU_PAGE_PROPERTY_UNKNOWN

The CPU-page property is unknown.


### -field D3D12_CPU_PAGE_PROPERTY_NOT_AVAILABLE


            The CPU cannot access the heap, therefore no page properties are available.
          


### -field D3D12_CPU_PAGE_PROPERTY_WRITE_COMBINE

The CPU-page property is write-combined.


### -field D3D12_CPU_PAGE_PROPERTY_WRITE_BACK

The CPU-page property is write-back.


## -remarks




        This enum is used by the <a href="https://msdn.microsoft.com/0A197D3D-67F4-46BB-8578-15E05DF46067">D3D12_HEAP_PROPERTIES</a> structure.
      




## -see-also




<a href="https://msdn.microsoft.com/76E76C85-128E-4F0E-9711-C72C4CF6C835">Core Enumerations</a>
 

 

