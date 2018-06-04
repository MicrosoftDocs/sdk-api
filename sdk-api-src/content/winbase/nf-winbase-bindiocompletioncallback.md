---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# BindIoCompletionCallback function


## -description


Associates the I/O completion port owned by the <a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">thread pool</a> with the specified file handle. On completion of an I/O request involving this file, a non-I/O worker thread will execute the specified callback function.


## -parameters




### -param FileHandle [in]

A handle to the file opened for overlapped I/O completion. This handle is returned by the 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, with the <b>FILE_FLAG_OVERLAPPED</b> flag.


### -param Function [in]

A pointer to the callback function to be executed in a non-I/O worker thread when the I/O operation is complete. This callback function must not call the 
<a href="https://msdn.microsoft.com/ae1ad0f3-67df-4573-af22-7086f0470361">TerminateThread</a> function.

For more information about the completion routine, see 
<a href="https://msdn.microsoft.com/574eccda-03eb-4e8a-9d74-cfaecc7312ce">FileIOCompletionRoutine</a>.


### -param Flags [in]

This parameter must be zero.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
the <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> function. The value returned is an <b>NTSTATUS</b> error code. To retrieve the corresponding system error code, use the <a href="https://msdn.microsoft.com/library/windows/hardware/ff553127">RtlNtStatusToDosError</a> function.




## -remarks



The callback function might not be executed if the process issues an asynchronous request on the file specified by the <i>FileHandle</i> parameter but the request returns immediately with an error code other than ERROR_IO_PENDING.

Be sure that the thread that initiates the asynchronous I/O request does not terminate before the request is completed. Also, if a function in a DLL is queued to a worker thread, be sure that the function in the DLL has completed execution before the DLL is unloaded.

The thread pool maintains an I/O completion port. When you call <b>BindIoCompletionCallback</b>, it associates the specified file with the thread pool's I/O completion port. Asynchronous requests on that file object will complete by posting to the completion port, where they will be picked up by thread pool worker threads. For callbacks that must issue an I/O request that completes as an asynchronous procedure call, the thread pool provides an I/O worker pool. The I/O worker threads do not wait on the completion port; they sleep in an alertable wait state so that I/O request packets that complete can wake them up. Both types of worker threads check whether there is I/O pending on them and if there is, they do not exit. For more information, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff540625">Asynchronous Procedure Calls</a>.

To compile an application that uses this function, define _WIN32_WINNT as 0x0500 or later. For more information, see 
<a href="https://msdn.microsoft.com/a4def563-8ddc-4630-ae8a-86c07cf98374">Using the Windows Headers</a>.




## -see-also




<a href="https://msdn.microsoft.com/574eccda-03eb-4e8a-9d74-cfaecc7312ce">FileIOCompletionRoutine</a>



<a href="https://msdn.microsoft.com/8c8e8af0-bf50-4a4b-945c-83bae1eff7dd">Process and Thread Functions</a>



<a href="https://msdn.microsoft.com/a5e52080-35d4-47f5-9050-90889e3bf2f8">Thread Pooling</a>
 

 

