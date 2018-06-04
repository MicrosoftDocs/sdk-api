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

# GetOldestEventLogRecord function


## -description


Retrieves the absolute record number of the oldest record in the specified event log.


## -parameters




### -param hEventLog [in]

A handle to the open event log. The 
<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a> or 
<a href="https://msdn.microsoft.com/cfef0912-9d35-44aa-a1d3-f9bb37213ce0">OpenBackupEventLog</a> function returns this handle.


### -param OldestRecord [out]

A pointer to a variable that receives the absolute record number of the oldest record in the specified event log.


## -returns




						If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The oldest record in an event log is not necessarily record number 1. For more information, see 
<a href="https://msdn.microsoft.com/73731505-97f5-4985-8d00-c6ce8604902d">Event Log Records</a>.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/e03d2ab5-50ea-4916-9774-850506714538">Querying for Event Information</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/fd5c12ec-3a3d-4b75-a573-0b27ae7a890b">Event Logging Functions</a>



<a href="https://msdn.microsoft.com/80cc8735-26a2-4ad3-a111-28f2c0c52e98">GetNumberOfEventLogRecords</a>



<a href="https://msdn.microsoft.com/cfef0912-9d35-44aa-a1d3-f9bb37213ce0">OpenBackupEventLog</a>



<a href="https://msdn.microsoft.com/6cd8797a-aeaf-4603-b43c-b1ff45b6200a">OpenEventLog</a>
 

 

