---
UID: NF:jobapi.IsProcessInJob
title: IsProcessInJob function (jobapi.h)
description: Determines whether the process is running in the specified job.
helpviewer_keywords: ["IsProcessInJob","IsProcessInJob function","_win32_isprocessinjob","base.isprocessinjob","jobapi/IsProcessInJob","winbase/IsProcessInJob"]
old-location: base\isprocessinjob.htm
tech.root: backup
ms.assetid: 0253071d-a3fa-4ab0-86a7-71350d9fc24e
ms.date: 12/05/2018
ms.keywords: IsProcessInJob, IsProcessInJob function, _win32_isprocessinjob, base.isprocessinjob, jobapi/IsProcessInJob, winbase/IsProcessInJob
req.header: jobapi.h
req.include-header: 
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
 - IsProcessInJob
 - jobapi/IsProcessInJob
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-job-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-Core-misc-l1-1-0.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - IsProcessInJob
---

# IsProcessInJob function


## -description

Determines whether the process is running in the specified job.

## -parameters

### -param ProcessHandle [in]

A handle to the process to be tested. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="/windows/desktop/ProcThread/process-security-and-access-rights">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.

### -param JobHandle [in, optional]

A handle to the job. If this parameter is NULL, the function tests if the process is running under any job.

If this parameter is not NULL, the handle must have the JOB_OBJECT_QUERY access right. For more information, see <a href="/windows/desktop/ProcThread/job-object-security-and-access-rights">Job Object Security and Access Rights</a>.

### -param Result [out]

A pointer to a value that receives TRUE if the process is running in the job, and FALSE otherwise.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

An application cannot obtain a handle to the job object in which it is running unless it has the name of the job object. However, an application can call the <a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a> function with NULL to obtain information about the job object.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="/windows/desktop/WinProg/using-the-windows-headers">Using the Windows Headers</a>.

## -see-also

<a href="/windows/desktop/api/jobapi2/nf-jobapi2-assignprocesstojobobject">AssignProcessToJobObject</a>



<a href="/windows/desktop/ProcThread/job-objects">Job Objects</a>



<a href="/windows/desktop/ProcThread/process-and-thread-functions">Process and Thread Functions</a>



<a href="/windows/desktop/api/jobapi2/nf-jobapi2-queryinformationjobobject">QueryInformationJobObject</a>