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

# ReadLogRestartArea function


## -description


    Returns the last restart area that is  written successfully  to the log associated with the marshaling area of  <a href="https://msdn.microsoft.com/deb5fd90-e987-4e5b-9740-6ecef8705557">WriteLogRestartArea</a>. The function also returns a read context that allows the caller to cursor backward or forward through a log from the restart record.

This read context is   useful when scanning through previous restart areas prior to the current one by invoking <a href="https://msdn.microsoft.com/f304dbb7-7d5c-403c-9418-60947cc4c3a1">ReadPreviousLogRestartArea</a>.


## -parameters




### -param pvMarshal [in]

A pointer to a   marshaling context that is  allocated by using the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param ppvRestartBuffer [out]

A pointer to a variable that receives a pointer to the restart data in the log I/O block.


### -param pcbRestartBuffer [out]

A pointer to a variable that receives the amount of restart data.


### -param plsn [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure that receives the log sequence  number (LSN) of the restart area.


### -param ppvContext [out]

A pointer to a variable that receives a pointer to a system-allocated read context  when a read is successful.  

If the function defers completion of an operation, it    returns a valid read-context pointer and an error status of <b>ERROR_IO_PENDING</b>.  On all other errors, the read-context pointer is <b>NULL</b>.  For more information about handling deferred completion of the function, see the Remarks section of this topic. 

After obtaining all requested log records, the client must pass  the read context to <a href="https://msdn.microsoft.com/fb0a4c4e-cdb7-4c42-9102-bc76b8b70193">TerminateReadLog</a> to free the associated memory. Failure to do so results in memory leakage.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time, or passed into more than one asynchronous read at a time.</div>
<div> </div>

### -param OPTIONAL

TBD




#### - pOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that is required for asynchronous operation. 

This parameter can be <b>NULL</b> if an asynchronous operation is not used.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following list identifies the  possible error codes:




## -remarks



The error message ERROR_LOG_BLOCK_INCOMPLETE is returned if the log block size specified by <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> is not large enough to hold a complete log block.

Typically, <b>ReadLogRestartArea</b> is  used only  during client restart, either after a crash or after a   normal  shutdown.  

If there is no restart area in the log,  <b>ReadLogRestartArea</b> fails  with the  code <b>ERROR_LOG_NO_RESTART</b>.

If <b>ReadLogRestartArea</b>   fails with an error code of <b>ERROR_IO_PENDING</b>, a pointer to a valid read context  is placed in the variable pointed to by the <i>ppvReadContext</i> parameter. 

To complete the log-record copy, the client should first synchronize its execution with deferred completion of the overlapped I/O operation by  calling  <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a>, or one of the synchronization <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>. For more information, see <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.

After <b>ReadLogRestartArea</b> completes asynchronously, the requested restart area  is  read from the disk, but a valid pointer to it is not   placed in <i>*ppvRestartBuffer</i>.  

To obtain a valid pointer, the client must call <a href="https://msdn.microsoft.com/f304dbb7-7d5c-403c-9418-60947cc4c3a1">ReadPreviousLogRestartArea</a>, which passes in the read-context pointer returned by <b>ReadLogRestartArea</b>.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time.<p class="note">CLFS read contexts should not be passed into more than one asynchronous read at a time, or the function fails with ERROR_BUSY.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/f304dbb7-7d5c-403c-9418-60947cc4c3a1">ReadPreviousLogRestartArea</a>



<a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>



<a href="https://msdn.microsoft.com/deb5fd90-e987-4e5b-9740-6ecef8705557">WriteLogRestartArea</a>
 

 

