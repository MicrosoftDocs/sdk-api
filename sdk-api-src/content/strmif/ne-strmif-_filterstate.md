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

# _FilterState enumeration


## -description



Specifies a filter's state or the state of the filter graph.




## -enum-fields




### -field State_Stopped

Stopped. The filter is not processing data.


### -field State_Paused

Paused. The filter is processing data, but not rendering it.


### -field State_Running

Running. The filter is processing and rendering data.


## -see-also




<a href="https://msdn.microsoft.com/3fcfd874-39bc-42d2-9fc9-2d8945ffa8e3">Data Flow in the Filter Graph</a>



<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/653a94ff-6929-41b1-9b94-dccaff0f7ec7">IMediaControl::GetState</a>



<a href="https://msdn.microsoft.com/b20ca3e9-bec2-4c6d-ba80-f4dae2f5a831">IMediaFilter::GetState</a>
 

 

