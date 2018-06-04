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

# _IO_COUNTERS structure


## -description


Contains I/O accounting information for a process or a job object. For a job object, the counters include all operations performed by all processes that have ever been associated with the job, in addition to all processes currently associated with the job.


## -struct-fields




### -field ReadOperationCount

The number of read operations performed.


### -field WriteOperationCount

The number of write operations performed.


### -field OtherOperationCount

The number of I/O operations performed, other than read and write operations.


### -field ReadTransferCount

The number of bytes read.


### -field WriteTransferCount

The number of bytes written.


### -field OtherTransferCount

The number of bytes transferred during operations other than read and write operations.


## -see-also




<a href="https://msdn.microsoft.com/e6973c1b-86bc-4fd1-aff6-26e87f8013c4">GetProcessIoCounters</a>



<a href="https://msdn.microsoft.com/5c3e4002-d4d2-4a8c-ab0c-f6bcdd62947a">JOBOBJECT_BASIC_AND_IO_ACCOUNTING_INFORMATION</a>
 

 

