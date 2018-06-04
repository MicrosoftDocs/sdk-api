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

# D3D12_BUFFER_UAV structure


## -description


Describes the elements in a buffer to use in a unordered-access view.


## -struct-fields




### -field FirstElement

The zero-based index of the first element to be accessed.


### -field NumElements

The number of elements in the resource. For structured buffers, this is the number of structures in the buffer.


### -field StructureByteStride

The size of each element in the buffer structure (in bytes) when the buffer represents a structured buffer.


### -field CounterOffsetInBytes


            The counter offset, in bytes.
          


### -field Flags


            A <a href="https://msdn.microsoft.com/D5350B5B-4E15-4B9F-B3E0-5A3B1592ED5C">D3D12_BUFFER_UAV_FLAGS</a>-typed value that specifies the view options for the resource.
          


## -remarks




        Use this structure with a <a href="https://msdn.microsoft.com/0C3A31FE-625D-4CB3-87FD-D2C33D008DD4">D3D12_UNORDERED_ACCESS_VIEW_DESC</a> structure to view the resource as a buffer.
      




## -see-also




<a href="https://msdn.microsoft.com/7FE8796A-98D1-4333-8755-2A47567460B3">Core Structures</a>
 

 

