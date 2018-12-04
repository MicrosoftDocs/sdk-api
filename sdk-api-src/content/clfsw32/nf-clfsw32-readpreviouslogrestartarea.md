---
UID: NF:clfsw32.ReadPreviousLogRestartArea
title: ReadPreviousLogRestartArea function
author: windows-sdk-content
description: Reads the previous log restart area that is relative to the current restart record specified in the read context, pvReadContext. This read context is the one previously created by a call to ReadLogRestartArea.
old-location: fs\readpreviouslogrestartarea.htm
tech.root: Clfs
ms.assetid: f304dbb7-7d5c-403c-9418-60947cc4c3a1
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ReadPreviousLogRestartArea, ReadPreviousLogRestartArea function [Files], clfsw32/ReadPreviousLogRestartArea, fs.readpreviouslogrestartarea
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - ReadPreviousLogRestartArea
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ReadPreviousLogRestartArea function


## -description


Reads the previous log restart area that is relative to the current restart record specified in the read context, <i>pvReadContext</i>. This read context is the one previously created by  a call to <a href="https://msdn.microsoft.com/ab59d2fe-d951-42f3-b270-844eaeb6ff90">ReadLogRestartArea</a>.


## -parameters




### -param pvReadContext [in]

A pointer to a system-allocated read context that <a href="https://msdn.microsoft.com/ab59d2fe-d951-42f3-b270-844eaeb6ff90">ReadLogRestartArea</a> returns.

  Even when those functions return <b>ERROR_IO_PENDING</b>, they still return a pointer to a valid read context. For information about  asynchronous completion, see the Remarks section of this topic.


### -param ppvRestartBuffer [out]

A pointer to a variable that receives a pointer to the restart data.


### -param pcbRestartBuffer [out]

A pointer to a variable that receives the size of the restart data at <i>*ppvRestartBuffer</i>, in bytes.


### -param plsnRestart [out]

A pointer to a <a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a> structure that receives the log sequence number (LSN) of the restart area  that   this function returns.


### -param pOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that  is required for asynchronous operation. 

This parameter can be <b>NULL</b> if asynchronous operation is not used.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following list identifies the possible error codes:




## -remarks



The error message ERROR_LOG_BLOCK_INCOMPLETE is returned if the log block size specified by <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> is not large enough to hold a complete log block.

If <b>ReadPreviousLogRestartArea</b>  fails with an error code of <b>ERROR_IO_PENDING</b>, a pointer to a valid read context  is placed in the variable that is pointed to by the <i>ppvReadContext</i> parameter.

To complete the log-record copy, the client should first synchronize its execution with deferred completion of the overlapped I/O operation by using <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or one of the synchronization <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>. For more information, see <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.

After <b>ReadPreviousLogRestartArea</b> completes asynchronously, the requested restart area is read from the disk, but a valid pointer to it is not  placed in <i>*ppvRestartBuffer</i>.

To obtain a valid pointer,  the client must call <b>ReadPreviousLogRestartArea</b> a second time.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time.<p class="note">CLFS read contexts should not be passed into more than one asynchronous read at a time, or the function fails with ERROR_READ.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/ac104bf9-7ca7-417a-bd14-09b0e82c6a77">CreateLogFile</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/ab59d2fe-d951-42f3-b270-844eaeb6ff90">ReadLogRestartArea</a>



<a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>
 

 

