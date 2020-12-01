---
UID: NF:jobapi2.TerminateJobObject
title: TerminateJobObject function (jobapi2.h)
description: Terminates all processes currently associated with the job.
helpviewer_keywords: ["TerminateJobObject","TerminateJobObject function","_win32_terminatejobobject","base.terminatejobobject","winbase/TerminateJobObject"]
old-location: base\terminatejobobject.htm
tech.root: backup
ms.assetid: ff8eb4a8-26d0-4f01-ab56-3c51fb16e87c
ms.date: 12/05/2018
ms.keywords: TerminateJobObject, TerminateJobObject function, _win32_terminatejobobject, base.terminatejobobject, winbase/TerminateJobObject
req.header: jobapi2.h
req.include-header: Windows.h, Jobapi2.h
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TerminateJobObject
 - jobapi2/TerminateJobObject
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
 - API-MS-Win-Core-Job-L2-1-1.dll
api_name:
 - TerminateJobObject
---

# TerminateJobObject function


## -description

Terminates all processes currently associated with the job.  If the job is nested, this function terminates all processes currently associated with the job and all of its child jobs in the hierarchy.

## -parameters

### -param hJob [in]

A handle to the job whose processes will be terminated. The 
<a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a> or 
<a href="/windows/desktop/api/winbase/nf-winbase-openjobobjecta">OpenJobObject</a> function returns this handle. This handle must have the JOB_OBJECT_TERMINATE access right. For more information, see 
<a href="/windows/desktop/ProcThread/job-object-security-and-access-rights">Job Object Security and Access Rights</a>.

The handle for each process in the job object must have the PROCESS_TERMINATE access right. For more information, see 
<a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

### -param uExitCode [in]

The exit code to be used by all processes and threads in the job object. Use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodeprocess">GetExitCodeProcess</a> function to retrieve each process's exit value. Use the 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-getexitcodethread">GetExitCodeThread</a> function to retrieve each thread's exit value.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

It is not possible for any of the processes associated with the job to postpone or handle the termination. It is as if 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a> were called for each process associated with the job.

Terminating a nested job additionally terminates all child job objects. Resources used by the terminated jobs are charged up the parent job chain in the hierarchy.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/winbase/nf-winbase-createjobobjecta">CreateJobObject</a>



<a href="/windows/desktop/ProcThread/job-objects">Job Objects</a>



<a href="/windows/desktop/api/winbase/nf-winbase-openjobobjecta">OpenJobObject</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-terminateprocess">TerminateProcess</a>