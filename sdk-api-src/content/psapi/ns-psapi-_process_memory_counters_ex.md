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

# _PROCESS_MEMORY_COUNTERS_EX structure


## -description


Contains extended memory statistics for a process.


## -struct-fields




### -field cb

The size of the structure, in bytes.


### -field PageFaultCount

The number of page faults.


### -field PeakWorkingSetSize

The peak working set size, in bytes.


### -field WorkingSetSize

The current working set size, in bytes.


### -field QuotaPeakPagedPoolUsage

The peak paged pool usage, in bytes.


### -field QuotaPagedPoolUsage

The current paged pool usage, in bytes.


### -field QuotaPeakNonPagedPoolUsage

The peak nonpaged pool usage, in bytes.


### -field QuotaNonPagedPoolUsage

The current nonpaged pool usage, in bytes.


### -field PagefileUsage

The Commit Charge value in bytes for this process. Commit Charge is the total amount of memory that the memory manager has committed for a running process.

<b>Windows 7 and Windows Server 2008 R2 and earlier:  </b><b>PagefileUsage</b> is always zero. Check <b>PrivateUsage</b> instead.


### -field PeakPagefileUsage

The peak value in bytes of the Commit Charge during the lifetime of this process.


### -field PrivateUsage

Same as <b>PagefileUsage</b>. The Commit Charge value in bytes for this process. Commit Charge is the total amount of memory that the memory manager has committed for a running process.


## -see-also




<a href="https://msdn.microsoft.com/12990e8d-6097-4502-824e-db6c3f76c715">GetProcessMemoryInfo</a>



<a href="https://msdn.microsoft.com/b27ca747-8fd2-4267-9979-4e2e14a5a19f">Memory Performance Information</a>



<a href="https://msdn.microsoft.com/683c899e-a7e8-4440-8f13-2a713c1618bf">Process Memory Usage Information</a>



<a href="https://msdn.microsoft.com/33c42f79-cc77-4d44-84c3-8bf0a4a60019">Working Set Information</a>
 

 

