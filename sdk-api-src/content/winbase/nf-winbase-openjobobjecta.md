---
UID: NF:winbase.OpenJobObjectA
title: OpenJobObjectA function
author: windows-sdk-content
description: Opens an existing job object.
old-location: base\openjobobject.htm
tech.root: procthread
ms.assetid: cb6ebc6f-5c61-408d-a781-ba029c83ddeb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: OpenJobObject, OpenJobObject function, OpenJobObjectA, OpenJobObjectW, _win32_openjobobject, base.openjobobject, winbase/OpenJobObject, winbase/OpenJobObjectA, winbase/OpenJobObjectW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h, Jobapi2.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: OpenJobObjectW (Unicode) and OpenJobObjectA (ANSI)
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
 - OpenJobObject
 - OpenJobObjectA
 - OpenJobObjectW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# OpenJobObjectA function


## -description


Opens an existing job object.


## -parameters




### -param dwDesiredAccess [in]

The access to the job object. This parameter can be one or more of the 
<a href="https://msdn.microsoft.com/8d212292-f087-41e4-884e-cec4423dac49">job object access rights</a>. This access right is checked against any security descriptor for the object.


### -param bInheritHandle [in]

If this value is TRUE, processes created by this process will inherit the handle. Otherwise, the processes do not inherit this handle.


### -param lpName [in]

The name of the job to be opened. Name comparisons are case sensitive.

This function can open objects in a private namespace. For more information, see <a href="https://msdn.microsoft.com/6a84ec16-fa65-4cdd-861a-eccf5d0eee2b">Object Namespaces</a>.

<b>Terminal Services:  </b>The name can have a "Global\" or "Local\" prefix to explicitly open the object in the global or session namespace. The remainder of the name can contain any character except the backslash character (\). For more information, see 
<a href="https://msdn.microsoft.com/771e0bbf-bd73-4e87-aa1e-945c1287b517">Kernel Object Namespaces</a>.


## -returns



If the function succeeds, the return value is a handle to the job. The handle provides the requested access to the job.

If the function fails, the return value is <b>NULL</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



To associate a process with a job, use the 
<a href="https://msdn.microsoft.com/f5d7a39f-6afe-4e4a-a802-e7f875ea6e5b">AssignProcessToJobObject</a> function.

To compile an application that uses this function, define <b>_WIN32_WINNT</b> as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/f5d7a39f-6afe-4e4a-a802-e7f875ea6e5b">AssignProcessToJobObject</a>



<a href="https://msdn.microsoft.com/59296384-5e78-44dd-8019-f1df6668928b">Job Objects</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>
 

 

