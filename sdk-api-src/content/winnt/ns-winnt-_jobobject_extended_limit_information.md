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

# _JOBOBJECT_EXTENDED_LIMIT_INFORMATION structure


## -description


Contains basic and extended limit information for a job object.


## -struct-fields




### -field BasicLimitInformation

A 
<a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure that contains basic limit information.


### -field IoInfo

Reserved.


### -field ProcessMemoryLimit

If the <b>LimitFlags</b> member of the 
<a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure specifies the <b>JOB_OBJECT_LIMIT_PROCESS_MEMORY</b> value, this member specifies the limit for the virtual memory that can be committed by a process. Otherwise, this member is ignored.


### -field JobMemoryLimit

If the <b>LimitFlags</b> member of the 
<a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a> structure specifies the <b>JOB_OBJECT_LIMIT_JOB_MEMORY</b> value, this member specifies the limit for the virtual memory that can be committed for the job. Otherwise, this member is ignored.


### -field PeakProcessMemoryUsed

The peak memory used by any process ever associated with the job.


### -field PeakJobMemoryUsed

The peak memory usage of all processes currently associated with the job.


## -remarks



The system tracks the value of <b>PeakProcessMemoryUsed</b> and <b>PeakJobMemoryUsed</b> constantly. This allows you know the peak memory usage of each job. You can use this information to establish a memory limit using the <b>JOB_OBJECT_LIMIT_PROCESS_MEMORY</b> or <b>JOB_OBJECT_LIMIT_JOB_MEMORY</b> value.

Note that the job memory and process memory limits are very similar in operation, but they are independent. You could set a job-wide limit of 100 MB with a per-process limit of 10 MB. In this scenario, no single process could commit more than 10 MB, and the set of processes associated with a job could never exceed 100 MB.

To register for notifications  that a job has exceeded its peak memory limit while allowing processes to continue to commit memory, use the <a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a> function with the <b>JobObjectNotificationLimitInformation</b> information class. 




## -see-also




<a href="https://msdn.microsoft.com/83b940a7-05a0-4f5e-bfe3-3f2ac17e2d67">JOBOBJECT_BASIC_LIMIT_INFORMATION</a>



<a href="https://msdn.microsoft.com/39cf5f26-dfc1-4f1d-aae4-5f29e277834f">JOBOBJECT_NOTIFICATION_LIMIT_INFORMATION</a>



<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>
 

 

