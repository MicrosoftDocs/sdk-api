---
UID: NF:winbase.CreateJobObjectA
title: CreateJobObjectA function
author: windows-sdk-content
description: Creates or opens a job object.
old-location: base\createjobobject.htm
tech.root: ProcThread
ms.assetid: ca6a044f-67ed-4a9c-9aeb-69dd77652854
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: CreateJobObject, CreateJobObject function, CreateJobObjectA, CreateJobObjectW, _win32_createjobobject, base.createjobobject, winbase/CreateJobObject, winbase/CreateJobObjectA, winbase/CreateJobObjectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateJobObjectW (Unicode) and CreateJobObjectA (ANSI)
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
 - API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
 - API-MS-Win-Core-Job-L2-1-1.dll
api_name:
 - CreateJobObject
 - CreateJobObjectA
 - CreateJobObjectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CreateJobObjectA function


## -description


Creates or opens a job object.


## -parameters




### -param lpJobAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that specifies the security descriptor for the job object and determines whether child processes can inherit the returned handle. If <i>lpJobAttributes</i> is <b>NULL</b>, the job object gets a default security descriptor and the handle cannot be inherited. The ACLs in the default security descriptor for a job object come from the primary or impersonation token of the creator.


### -param lpName [in, optional]

The name of the job. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case-sensitive. 




If <i>lpName</i> is <b>NULL</b>, the job is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, mutex, waitable timer, or file-mapping object, the function fails and the 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The object can be created in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>.


## -returns



If the function succeeds, the return value is a handle to the job object. The handle has the <b>JOB_OBJECT_ALL_ACCESS</b> access right. If the object existed before the function call, the function returns a handle to the existing job object and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is NULL. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When a job is created, its accounting information is initialized to zero, all limits are inactive, and there are no associated processes. To assign a process to  a job object, use the 
<a href="https://msdn.microsoft.com/f5d7a39f-6afe-4e4a-a802-e7f875ea6e5b">AssignProcessToJobObject</a> function. To set limits for a job, use the 
<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a> function. To query accounting information, use the 
<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a> function.

All processes associated with a job must run in the same session. A job is associated with the session of the first process to be assigned to the job.

<b>Windows Server 2003 and Windows XP:  </b>A job is associated with the session of the  process that created it.

To close a job object handle, use the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function. The job is destroyed when its last handle has been closed and all associated processes have exited. However, if the job has the <b>JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE</b> flag specified, closing the last job object handle terminates all associated processes and then destroys the job object itself.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5d7a39f-6afe-4e4a-a802-e7f875ea6e5b">AssignProcessToJobObject</a>



<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/59296384-5e78-44dd-8019-f1df6668928b">Job Objects</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/46f7c579-e8d3-4434-a6ce-56573cd84387">SetInformationJobObject</a>
 

 

