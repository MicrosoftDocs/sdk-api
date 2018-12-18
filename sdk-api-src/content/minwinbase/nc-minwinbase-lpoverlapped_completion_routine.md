---
UID: NC:minwinbase.LPOVERLAPPED_COMPLETION_ROUTINE
title: LPOVERLAPPED_COMPLETION_ROUTINE
author: windows-sdk-content
description: An application-defined callback function used with the ReadFileEx and WriteFileEx functions. It is called when the asynchronous input and output (I/O) operation is completed or canceled and the calling thread is in an alertable state.
old-location: fs\fileiocompletionroutine.htm
tech.root: fileio
ms.assetid: 574eccda-03eb-4e8a-9d74-cfaecc7312ce
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FileIOCompletionRoutine, FileIOCompletionRoutine callback, FileIOCompletionRoutine callback function [Files], LPOVERLAPPED_COMPLETION_ROUTINE, LPOVERLAPPED_COMPLETION_ROUTINE callback function [Files], _win32_fileiocompletionroutine, base.fileiocompletionroutine, fs.fileiocompletionroutine, minwinbase/FileIOCompletionRoutine, minwinbase/LPOVERLAPPED_COMPLETION_ROUTINE
ms.topic: callback
req.header: minwinbase.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - minwinbase.h
api_name:
 - FileIOCompletionRoutine
 - LPOVERLAPPED_COMPLETION_ROUTINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LPOVERLAPPED_COMPLETION_ROUTINE callback function


## -description


An application-defined callback function used with the 
    <a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a> and 
    <a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a> functions. It is called when the asynchronous 
    input and output (I/O) operation is completed or canceled and the calling thread is in an alertable 
    state (by using the <a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a>, 
    <a href="https://msdn.microsoft.com/1774b721-3ad4-492e-96af-b71de9066f0c">MsgWaitForMultipleObjectsEx</a>, 
    <a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a>, or 
    <a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a> function with the 
    <i>fAlertable</i> parameter set to <b>TRUE</b>).

The <b>LPOVERLAPPED_COMPLETION_ROUTINE</b> type defines a pointer to this callback 
    function. <b>FileIOCompletionRoutine</b> is a 
    placeholder for the application-defined function name.


## -parameters




### -param dwErrorCode [in]

The I/O completion status. This parameter can be one of the 
      <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>.


### -param dwNumberOfBytesTransfered [in]

The number of bytes transferred. If an error occurs, this parameter is zero.


### -param lpOverlapped [in, out]

A pointer to the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure specified by 
       the asynchronous I/O function.

The system does not use the <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure 
       after the completion routine is called, so the completion routine can deallocate the memory used by the 
       overlapped structure.


## -returns



This function does not return a value.




## -remarks



The return value for an asynchronous operation is 0 (<b>ERROR_SUCCESS</b>) if the operation 
    completed successfully or if the operation completed with a warning. To determine whether an I/O operation was 
    completed successfully, check that <i>dwErrorCode</i> is 0, call 
    <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>, then call 
    <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For example, if the buffer was not large 
    enough to receive all of the data from a call to <a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>, 
    <i>dwErrorCode</i> is set to 0, 
    <b>GetOverlappedResult</b> fails, and 
    <b>GetLastError</b> returns 
    <b>ERROR_MORE_DATA</b>.

Returning from this function allows another pending I/O completion routine to be called. All waiting 
    completion routines are called before the alertable thread's wait is completed with a return code of 
    <b>WAIT_IO_COMPLETION</b>. The system may call the waiting completion routines in any order. 
    They may or may not be called in the order the I/O functions are completed.

Each time the system calls a completion routine, it uses some of the application's stack. If the completion 
    routine does additional asynchronous I/O and alertable waits, the stack may grow.

For more information, see 
    <a href="https://msdn.microsoft.com/0197d78e-a4dc-414b-88ba-c5ec5f2ed614">Asynchronous Procedure Calls</a>.


#### Examples

For  example code, see 
     <a href="https://msdn.microsoft.com/8b73485c-c6f7-44df-9e53-308df2c752e7">Named Pipe Server Using Completion Routines</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/2eb18e84-6d6b-4b11-8e8f-6110fa44b7f9">BindIoCompletionCallback</a>



<a href="https://msdn.microsoft.com/1cf0547d-54ac-410a-acbe-7b3b3ebb310b">File Management Functions</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/6c1a4de1-6cae-4c35-bfba-0bc252fadbd9">ReadFileEx</a>



<a href="https://msdn.microsoft.com/a73cff94-ad63-4110-9f01-6469481c3d55">SleepEx</a>



<a href="https://msdn.microsoft.com/ade51d98-cc9d-4b33-9c52-559a9cb14707">Synchronous and Asynchronous I/O</a>



<a href="https://msdn.microsoft.com/47a167fb-4714-4353-b924-a161f367673c">WaitForMultipleObjectsEx</a>



<a href="https://msdn.microsoft.com/530b5340-f8b2-4e00-a3ca-87a7c7372482">WaitForSingleObjectEx</a>



<a href="https://msdn.microsoft.com/6995c4ee-ba91-41d5-b72d-19dc2eb95945">WriteFileEx</a>
 

 

