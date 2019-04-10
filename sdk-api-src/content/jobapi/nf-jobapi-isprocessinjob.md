---
UID: NF:jobapi.IsProcessInJob
title: IsProcessInJob function (jobapi.h)
author: windows-sdk-content
description: Determines whether the process is running in the specified job.
old-location: base\isprocessinjob.htm
tech.root: ProcThread
ms.assetid: 0253071d-a3fa-4ab0-86a7-71350d9fc24e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IsProcessInJob, IsProcessInJob function, _win32_isprocessinjob, base.isprocessinjob, jobapi/IsProcessInJob, winbase/IsProcessInJob
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IsProcessInJob function


## -description


Determines whether the process is running in the specified job.


## -parameters




### -param ProcessHandle [in]

A handle to the process to be tested. The handle must have the PROCESS_QUERY_INFORMATION or PROCESS_QUERY_LIMITED_INFORMATION access right. For more information, see <a href="https://msdn.microsoft.com/508a17c4-88cd-431a-a102-00180a7f7ab5">Process Security and Access Rights</a>.

<b>Windows Server 2003 and Windows XP:  </b>The handle must have the PROCESS_QUERY_INFORMATION access right.


### -param JobHandle [in, optional]

A handle to the job. If this parameter is NULL, the function tests if the process is running under any job.

If this parameter is not NULL, the handle must have the JOB_OBJECT_QUERY access right. For more information, see <a href="https://msdn.microsoft.com/8d212292-f087-41e4-884e-cec4423dac49">Job Object Security and Access Rights</a>.


### -param Result [out]

A pointer to a value that receives TRUE if the process is running in the job, and FALSE otherwise.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



An application cannot obtain a handle to the job object in which it is running unless it has the name of the job object. However, an application can call the <a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a> function with NULL to obtain information about the job object.

To compile an application that uses this function, define _WIN32_WINNT as 0x0501 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5d7a39f-6afe-4e4a-a802-e7f875ea6e5b">AssignProcessToJobObject</a>



<a href="https://msdn.microsoft.com/59296384-5e78-44dd-8019-f1df6668928b">Job Objects</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/d843d578-fd67-4708-959f-00245ff70ec6">QueryInformationJobObject</a>
 

 

