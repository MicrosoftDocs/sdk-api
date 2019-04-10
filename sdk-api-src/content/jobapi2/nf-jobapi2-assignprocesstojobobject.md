---
UID: NF:jobapi2.AssignProcessToJobObject
title: AssignProcessToJobObject function (jobapi2.h)
author: windows-sdk-content
description: Assigns a process to an existing job object.
old-location: base\assignprocesstojobobject.htm
tech.root: ProcThread
ms.assetid: f5d7a39f-6afe-4e4a-a802-e7f875ea6e5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AssignProcessToJobObject, AssignProcessToJobObject function, _win32_assignprocesstojobobject, base.assignprocesstojobobject, jobapi2/AssignProcessToJobObject
ms.topic: function
req.header: jobapi2.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-job-l2-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Job-L2-1-1.dll
api_name:
 - AssignProcessToJobObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AssignProcessToJobObject function


## -description


Assigns a process to an existing job object.


## -parameters




### -param hJob [in]

A handle to the job object to which the process will be associated. The 
<a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a> or 
<a href="https://msdn.microsoft.com/cb6ebc6f-5c61-408d-a781-ba029c83ddeb">OpenJobObject</a> function returns this handle. The handle must have the JOB_OBJECT_ASSIGN_PROCESS access right. For more information, see 
<a href="https://msdn.microsoft.com/8d212292-f087-41e4-884e-cec4423dac49">Job Object Security and Access Rights</a>.


### -param hProcess [in]

A handle to the process to associate with the job object. The handle must have the PROCESS_SET_QUOTA and PROCESS_TERMINATE access rights. For more information, see 
<a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

If the process is already associated with a job, the job specified by <i>hJob</i> must be empty or it must be in the hierarchy of nested jobs to which the process already belongs, and it cannot have UI limits set (<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a> with <b>JobObjectBasicUIRestrictions</b>). For more information, see Remarks. 

<b>Windows 7, Windows Server 2008 R2, Windows XP with SP3, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>The process must not already be assigned to a job; if it is, the function fails with ERROR_ACCESS_DENIED. This behavior changed starting in Windows 8 and Windows Server 2012.

<b>Terminal Services:  </b>All processes within a job must run within the same session as the job.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



After you associate a process with a job object using 
<b>AssignProcessToJobObject</b>, the process is subject to the limits set for the job. To set limits for a job, use the 
<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a> function.

If the job has a user-mode time limit, and the time limit has been exhausted, 
<b>AssignProcessToJobObject</b> fails and the specified process is terminated. If the time limit would be exceeded by associating the process, 
<b>AssignProcessToJobObject</b> still succeeds. However, the time limit violation will be reported. If the job has an active process limit, and the limit would be exceeded by associating this process, 
<b>AssignProcessToJobObject</b> fails, and the specified process is terminated.

Memory operations performed by a process associated with a job that has a memory limit are subject to the memory limit. Memory operations performed by the process before it was associated with the job are not examined by 
<b>AssignProcessToJobObject</b>.

If the process is already running and the job has security limitations, 
<b>AssignProcessToJobObject</b> may fail. For example, if the primary token of the process contains the local administrators group, but the job object has the security limitation JOB_OBJECT_SECURITY_NO_ADMIN, the function fails. If the job has the security limitation JOB_OBJECT_SECURITY_ONLY_TOKEN, the process must be created suspended. To create a suspended process, call the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function with the CREATE_SUSPENDED flag.

A process can be associated with more than one job in a hierarchy of nested jobs. For priority class, affinity, commit charge, per-process execution time limit, scheduling class limit, and working set minimum and maximum, the process inherits an effective limit which is the most restrictive limit of all the jobs in its parent job chain. For other resource limits, the process inherits limits from its immediate job in the hierarchy. Accounting information is added to the  immediate job and aggregated in each parent job in the job chain. By default, all child processes are associated with the immediate job and every job in the parent job chain. To create a child process that is not part of the same job chain, call the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function with the CREATE_BREAKAWAY_FROM_JOB flag. The child process breaks away from every job in the job chain unless a job in the chain does not allow breakaway. In this case, the child process does not break away from that job or any job above it in the job chain. For more information, see <a href="https://msdn.microsoft.com/FA22493B-CD29-49A7-BDAC-349FA96B8C9E">Nested Jobs</a>. 

<b>Windows 7, Windows Server 2008 R2, Windows XP with SP3, Windows Server 2008, Windows Vista and Windows Server 2003:  </b>A process can be associated only with a single job. A process inherits limits from the job it is associated with and adds its accounting information to the job. If a process is associated with a job, all child processes it creates are associated with that job by default. To create a child process that is not part of the same job, call the 
<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function with the CREATE_BREAKAWAY_FROM_JOB flag. A process can be associated with more than one job starting in Windows 8 and Windows Server 2012.

<b>Windows 7, Windows Server 2008 R2, Windows Server 2008 and Windows Vista:  </b>If the process is being monitored by the Program Compatibility Assistant (PCA), it is placed into a compatibility job. Therefore, the process must be created using CREATE_BREAKAWAY_FROM_JOB before it can be placed in another job. Alternatively, you can embed an application manifest that specifies a User Account Control (UAC) level in your application and PCA will not add the process to the compatibility job. For more information, see <a href="http://go.microsoft.com/fwlink/p/?linkid=102463">Application Development Requirements for User Account Control Compatibility</a>.

If the job or any of its parent jobs in the job chain is terminating when <b>AssignProcessToJob</b> is called, the function fails.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/ca6a044f-67ed-4a9c-9aeb-69dd77652854">CreateJobObject</a>



<a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a>



<a href="https://msdn.microsoft.com/59296384-5e78-44dd-8019-f1df6668928b">Job Objects</a>



<a href="https://msdn.microsoft.com/cb6ebc6f-5c61-408d-a781-ba029c83ddeb">OpenJobObject</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>
 

 

