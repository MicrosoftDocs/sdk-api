---
UID: NF:winbase.BindIoCompletionCallback
title: BindIoCompletionCallback function
author: windows-sdk-content
description: Associates the I/O completion port owned by the thread pool with the specified file handle. On completion of an I/O request involving this file, a non-I/O worker thread will execute the specified callback function.
old-location: base\bindiocompletioncallback.htm
old-project: procthread
ms.assetid: 2eb18e84-6d6b-4b11-8e8f-6110fa44b7f9
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: BindIoCompletionCallback, BindIoCompletionCallback function, _win32_bindiocompletioncallback, base.bindiocompletioncallback, winbase/BindIoCompletionCallback
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.redist: 
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
tech.root: 
req.typenames: PRIORITY_HINT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - BindIoCompletionCallback
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# BindIoCompletionCallback function


## -description


Associates the I/O completion port owned by the <a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">thread pool</a> with the specified file handle. On completion of an I/O request involving this file, a non-I/O worker thread will execute the specified callback function.


## -parameters




### -param FileHandle [in]

A handle to the file opened for overlapped I/O completion. This handle is returned by the 
<a href="https://msdn.microsoft.com/en-us/library/Aa363858(v=VS.85).aspx">CreateFile</a> function, with the <b>FILE_FLAG_OVERLAPPED</b> flag.


### -param Function [in]

A pointer to the callback function to be executed in a non-I/O worker thread when the I/O operation is complete. This callback function must not call the 
<a href="https://msdn.microsoft.com/ae1ad0f3-67df-4573-af22-7086f0470361">TerminateThread</a> function.

For more information about the completion routine, see 
<a href="https://msdn.microsoft.com/en-us/library/Aa364052(v=VS.85).aspx">FileIOCompletionRoutine</a>.


### -param Flags [in]

This parameter must be zero.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. The value returned is an <b>NTSTATUS</b> error code. To retrieve the corresponding system error code, use the <a href="https://msdn.microsoft.com/4a28be1f-28b9-45a4-8ac7-58e43452558a">RtlNtStatusToDosError</a> function.




## -remarks



The callback function might not be executed if the process issues an asynchronous request on the file specified by the <i>FileHandle</i> parameter but the request returns immediately with an error code other than ERROR_IO_PENDING.

Be sure that the thread that initiates the asynchronous I/O request does not terminate before the request is completed. Also, if a function in a DLL is queued to a worker thread, be sure that the function in the DLL has completed execution before the DLL is unloaded.

The thread pool maintains an I/O completion port. When you call <b>BindIoCompletionCallback</b>, it associates the specified file with the thread pool's I/O completion port. Asynchronous requests on that file object will complete by posting to the completion port, where they will be picked up by thread pool worker threads. For callbacks that must issue an I/O request that completes as an asynchronous procedure call, the thread pool provides an I/O worker pool. The I/O worker threads do not wait on the completion port; they sleep in an alertable wait state so that I/O request packets that complete can wake them up. Both types of worker threads check whether there is I/O pending on them and if there is, they do not exit. For more information, see <a href="https://msdn.microsoft.com/0197d78e-a4dc-414b-88ba-c5ec5f2ed614">Asynchronous Procedure Calls</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa364052(v=VS.85).aspx">FileIOCompletionRoutine</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">Thread Pooling</a>
 

 

