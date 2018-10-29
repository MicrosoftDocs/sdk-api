---
UID: NS:winnt._JOBOBJECT_EXTENDED_LIMIT_INFORMATION
title: "_JOBOBJECT_EXTENDED_LIMIT_INFORMATION"
author: windows-sdk-content
description: Contains basic and extended limit information for a job object.
old-location: base\jobobject_extended_limit_information_str.htm
tech.root: ProcThread
ms.assetid: 5712fd27-6489-4fdc-b69b-4fb6a7c52c02
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PJOBOBJECT_EXTENDED_LIMIT_INFORMATION, JOBOBJECT_EXTENDED_LIMIT_INFORMATION, JOBOBJECT_EXTENDED_LIMIT_INFORMATION structure, PJOBOBJECT_EXTENDED_LIMIT_INFORMATION, PJOBOBJECT_EXTENDED_LIMIT_INFORMATION structure pointer, _JOBOBJECT_EXTENDED_LIMIT_INFORMATION, _win32_jobobject_extended_limit_information_str, base.jobobject_extended_limit_information_str, winnt/JOBOBJECT_EXTENDED_LIMIT_INFORMATION, winnt/PJOBOBJECT_EXTENDED_LIMIT_INFORMATION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: winnt.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WinNT.h
api_name:
 - JOBOBJECT_EXTENDED_LIMIT_INFORMATION
product: Windows
targetos: Windows
req.typenames: JOBOBJECT_EXTENDED_LIMIT_INFORMATION, *PJOBOBJECT_EXTENDED_LIMIT_INFORMATION
req.redist: 
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
 

 

