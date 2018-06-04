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

# _PERF_COUNTERSET_INSTANCE structure


## -description


Defines an instance of a counter set. 


## -struct-fields




### -field CounterSetGuid

GUID that identifies the counter set to which this instance belongs.


### -field dwSize

Size, in bytes, of the instance block. The instance block contains this structure, followed by one or more <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> blocks, and ends with the instance name.


### -field InstanceId

Identifier that uniquely identifies this instance. 

The provider specified the identifier when calling <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>.


### -field InstanceNameOffset

Byte offset from the beginning of this structure to the null-terminated Unicode instance name.

The provider specified the instance name when calling <a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>.


### -field InstanceNameSize

Size, in bytes, of the instance name. The size includes the null-terminator.


## -remarks



The <b>Offset</b> member of  <a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a> contains the byte offset from the beginning of the <b>PERF_COUNTERSET_INSTANCE</b> block to the counter's raw counter value.




## -see-also




<a href="https://msdn.microsoft.com/f1fb6ad5-ad38-46d0-b76d-803887ba3d97">PERF_COUNTER_INFO</a>



<a href="https://msdn.microsoft.com/73be8588-2c87-4c27-933d-62b8605ed9a3">PerfCreateInstance</a>



<a href="https://msdn.microsoft.com/8266e58c-c0a3-42dd-9f06-0d04dccfcf7c">PerfDeleteInstance</a>



<a href="https://msdn.microsoft.com/844f3f9e-8de2-4995-b13c-befe0da8a1ab">PerfQueryInstance</a>
 

 

