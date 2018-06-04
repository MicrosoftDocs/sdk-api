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

# IDataCollectorSet::get_StopOnCompletion


## -description


Retrieves or sets a value that determines whether the data collector set stops when all the data collectors in the set are in a completed state.

This property is read/write.


## -parameters


## -remarks



A data collector set stops only after all the data collectors in the set are complete. The following table identifies when each data collector is complete.

<table>
<tr>
<th>Collector</th>
<th>Is complete </th>
</tr>
<tr>
<td>Configuration</td>
<td>When all configuration information has been collected.</td>
</tr>
<tr>
<td>Performance Counter and Event Tracing</td>
<td>Immediately if both <a href="https://msdn.microsoft.com/d958c7a7-0258-4db6-b650-14a61d59221b">segment duration</a> and <a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">segment size</a> are zero. Otherwise, if either segment duration or segment size is specified, then the set completes only after one of the segment conditions is met.For Performance Counter, the <a href="https://msdn.microsoft.com/cc987959-dbf6-44da-8f1a-d66a3ad791a5">maximum number of records segment</a> is also considered.

</td>
</tr>
<tr>
<td>Alert and API Tracing</td>
<td>Immediately. </td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/6654c101-5179-41db-8fd9-ae281691073f">IDataCollectorSet::Schedules</a>



<a href="https://msdn.microsoft.com/b869ea8e-4fc8-4974-9e1c-1d2c480c3b0e">IDataCollectorSet::Stop</a>
 

 

