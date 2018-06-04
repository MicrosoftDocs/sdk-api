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

# _PERF_COUNTER_BLOCK structure


## -description



			Describes the block of memory that contains the raw performance counter data for an 
object's counters.
		


## -struct-fields




### -field ByteLength

Size of this structure and the raw counter data that follows, in bytes.


## -remarks



The <b>CounterOffset</b> member of <a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a> provides the offset from the beginning of this structure to the counter value.

The location of the <b>PERF_COUNTER_BLOCK</b> structure within the <a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a> block depends on if the object contains instances. For details, see <a href="https://msdn.microsoft.com/a68fa617-834c-4ad9-b922-fac3a648ad75">Performance Data Format</a>.

You must ensure that the size of the counter block is aligned to an 8-byte boundary. For example, if the performance object includes two DWORD counters, you must add an additional four bytes to the counter block to make it aligned to an 8-byte boundary.




## -see-also




<a href="https://msdn.microsoft.com/faef043b-81e0-49b0-913f-d691bafd17e6">PERF_COUNTER_DEFINITION</a>



<a href="https://msdn.microsoft.com/5ea617d3-857d-4e0a-ad10-4d63044fc927">PERF_INSTANCE_DEFINITION</a>



<a href="https://msdn.microsoft.com/9ed4f890-6256-45fd-a310-b5963a6131ae">PERF_OBJECT_TYPE</a>
 

 

