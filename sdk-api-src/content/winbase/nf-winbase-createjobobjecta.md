---
UID: NF:winbase.CreateJobObjectA
title: CreateJobObjectA function (winbase.h)
description: Creates or opens a job object. (CreateJobObjectA)
helpviewer_keywords: ["CreateJobObject","CreateJobObject function","CreateJobObjectA","CreateJobObjectW","_win32_createjobobject","base.createjobobject","winbase/CreateJobObject","winbase/CreateJobObjectA","winbase/CreateJobObjectW"]
old-location: base\createjobobject.htm
tech.root: backup
ms.assetid: ca6a044f-67ed-4a9c-9aeb-69dd77652854
ms.date: 12/05/2018
ms.keywords: CreateJobObject, CreateJobObject function, CreateJobObjectA, CreateJobObjectW, _win32_createjobobject, base.createjobobject, winbase/CreateJobObject, winbase/CreateJobObjectA, winbase/CreateJobObjectW
req.header: winbase.h
req.include-header: Windows.h, Jobapi2.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateJobObjectA
 - winbase/CreateJobObjectA
dev_langs:
 - c++
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
---

# CreateJobObjectA function


## -description

Creates or opens a job object.

## -parameters

### -param lpJobAttributes [in, optional]

A pointer to a 
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure that specifies the security descriptor for the job object and determines whether child processes can inherit the returned handle. If <i>lpJobAttributes</i> is <b>NULL</b>, the job object gets a default security descriptor and the handle cannot be inherited. The ACLs in the default security descriptor for a job object come from the primary or impersonation token of the creator.

### -param lpName [in, optional]

The name of the job. The name is limited to <b>MAX_PATH</b> characters. Name comparison is case-sensitive. 




If <i>lpName</i> is <b>NULL</b>, the job is created without a name.

If <i>lpName</i> matches the name of an existing event, semaphore, mutex, waitable timer, or file-mapping object, the function fails and the 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> function returns <b>ERROR_INVALID_HANDLE</b>. This occurs because these objects share the same namespace.

The object can be created in a private namespace. For more information, see <a href="/windows/desktop/Sync/object-namespaces">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly create the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\\). For more information, see 
<a href="/windows/desktop/TermServ/kernel-object-namespaces">Kernel Object Namespaces</a>.

## -returns

If the function succeeds, the return value is a handle to the job object. The handle has the <b>JOB_OBJECT_ALL_ACCESS</b> access right. If the object existed before the function call, the function returns a handle to the existing job object and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_ALREADY_EXISTS</b>.

If the function fails, the return value is NULL. To get extended error information, call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

When a job is created, its accounting information is initialized to zero, all limits are inactive, and there are no associated processes. To assign a process to  a job object, use the 
<a href="/windows/desktop/api/jobapi2/nf-jobapi2-assignprocesstojobobject">AssignProcessToJobObject</a> function. To set limits for a job, use the 
<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a> function. To query accounting information, use the 
<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> function.

All processes associated with a job must run in the same session. A job is associated with the session of the first process to be assigned to the job.

<b>Windows Server 2003 and Windows XP:  </b>A job is associated with the session of the  process that created it.

To close a job object handle, use the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function. The job is destroyed when its last handle has been closed and all associated processes have exited. However, if the job has the <b>JOB_OBJECT_LIMIT_KILL_ON_JOB_CLOSE</b> flag specified, closing the last job object handle terminates all associated processes and then destroys the job object itself.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-assignprocesstojobobject">AssignProcessToJobObject</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/ProcThread/job-objects">Job Objects</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-setinformationjobobject">SetInformationJobObject</a>
