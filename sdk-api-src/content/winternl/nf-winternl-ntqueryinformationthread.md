---
UID: NF:winternl.NtQueryInformationThread
title: NtQueryInformationThread function (winternl.h)
author: windows-sdk-content
description: Retrieves information about the specified thread.
old-location: base\ntqueryinformationthread.htm
tech.root: ProcThread
ms.assetid: ca292efc-1ea9-4c0f-b0a7-1cfb35d69f81
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: NtQueryInformationThread, NtQueryInformationThread function, base.ntqueryinformationthread, winternl/NtQueryInformationThread
ms.topic: function
req.header: winternl.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: Ntdll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntdll.dll
api_name:
 - NtQueryInformationThread
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NtQueryInformationThread function


## -description


<p class="CCE_Message">[<b>NtQueryInformationThread</b> may be altered or unavailable in future versions of Windows. Applications should use the alternate functions listed in this topic.]

Retrieves  information about the specified thread.


## -parameters




### -param ThreadHandle [in]

A handle to the thread about which information is being requested.


### -param ThreadInformationClass [in]

If this parameter is the <b>ThreadIsIoPending</b> value of the  <b>THREADINFOCLASS</b> enumeration, the function determines whether the thread has any I/O operations pending.

Use the public  function <a href="https://msdn.microsoft.com/5502f735-38f5-44a4-908d-1b421ee66aec">GetThreadIOPendingFlag</a> instead to obtain this information.

If this parameter is the <b>ThreadQuerySetWin32StartAddress</b> value of the <b>THREADINFOCLASS</b> enumeration, the function returns the start address of the thread. Note that on versions of Windows prior to Windows Vista, the returned start address is only reliable before the thread starts running.

If this parameter is the <b>ThreadSubsystemInformation</b> value of the  <b>THREADINFOCLASS</b> enumeration, the function retrieves a <a href="https://msdn.microsoft.com/B1E334BF-AAB3-410D-8D10-A750E8459E42">SUBSYSTEM_INFORMATION_TYPE</a> value indicating the subsystem type of the thread. The buffer pointed to by the <i>ThreadInformation</i> parameter should be large enough to hold a single <b>SUBSYSTEM_INFORMATION_TYPE</b> enumeration.


### -param ThreadInformation [in, out]

A pointer to a buffer in which the function writes the requested information. If <b>ThreadIsIoPending</b> is specified for the <i>ThreadInformationClass</i> parameter, this buffer must be large enough to hold a <b>ULONG</b> value, which indicates whether  the specified thread has I/O requests pending. If this value is equal to zero, then there are no I/O operations pending; otherwise, if the value is nonzero, then the thread does have I/O operations pending.

Use the public  function <a href="https://msdn.microsoft.com/5502f735-38f5-44a4-908d-1b421ee66aec">GetThreadIOPendingFlag</a> instead to obtain this information.

If <b>ThreadQuerySetWin32StartAddress</b> is specified for the <i>ThreadInformationClass</i> parameter, this buffer must be large enough to hold a PVOID value, which is the start address of the thread.


### -param ThreadInformationLength [in]

The size of the buffer pointed to by the <i>ThreadInformation</i> parameter, in bytes.


### -param ReturnLength [out, optional]

A pointer to a variable in which the function returns the size of the requested information. If the function was successful, this is the size of the information written to the buffer pointed to by the <i>ThreadInformation</i> parameter, but if the buffer was too small, this is the minimum size of buffer required to receive the information successfully.


## -returns



Returns an NTSTATUS success or error code. 

The forms and significance of NTSTATUS error codes are listed in the Ntstatus.h header file available in the DDK, and are described in the DDK documentation under Kernel-Mode Driver Architecture / Design Guide / Driver Programming Techniques / Logging Errors.




## -remarks



The <b>NtQueryInformationThread</b> function is internal to the operating system and  subject to change from one  release of Windows to another.  To maintain the    compatibility of your application, it is better to use the public  function previously mentioned instead.

If you do use <b>NtQueryInformationThread</b>, access the function through <a href="https://msdn.microsoft.com/0ffce2b1-ce50-4550-aa68-6628fdcac01a">run-time dynamic linking</a>.  This gives  your code an opportunity to respond gracefully if the function has been   changed or removed from the operating system. Signature changes, however, may not be detectable.

This function has no associated import library. You must use the <a href="https://msdn.microsoft.com/d936b4dd-058c-48e1-834b-b47ef6d8ef65">LoadLibrary</a> and <a href="https://msdn.microsoft.com/a0d7fc09-f888-4f46-a571-d3719a627597">GetProcAddress</a> functions to dynamically link to Ntdll.dll.




## -see-also




<a href="https://msdn.microsoft.com/5502f735-38f5-44a4-908d-1b421ee66aec">GetThreadIOPendingFlag</a>
 

 

