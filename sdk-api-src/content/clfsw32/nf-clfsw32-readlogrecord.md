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

# ReadLogRecord function


## -description


Initiates a sequence of reads from a specified log sequence number (LSN) in one of three modes, and returns the first of the specified log records and a read context.  A client can read subsequent records in the designated mode by passing the read context to <a href="https://msdn.microsoft.com/7736106b-6c43-496e-83b8-fa433c29e680">ReadNextLogRecord</a>.


## -parameters




### -param pvMarshal [in]

A pointer to a  marshaling context that is allocated by using the <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> function.


### -param plsnFirst [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure that specifies the log sequence number (LSN) of the record  where  the read operation should start.  

This value must be an LSN of a valid record in the active range of the log.


### -param eContextMode [in]

The mode for the read context that is returned in <i>*ppvReadContext</i>.  

The following table identifies the three  mutually exclusive  read modes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsContextPrevious"></a><a id="clfscontextprevious"></a><a id="CLFSCONTEXTPREVIOUS"></a><dl>
<dt><b>ClfsContextPrevious</b></dt>
</dl>
</td>
<td width="60%">
 Reads the  record linked to by <i>plsnPrevious</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsContextUndoNext"></a><a id="clfscontextundonext"></a><a id="CLFSCONTEXTUNDONEXT"></a><dl>
<dt><b>ClfsContextUndoNext</b></dt>
</dl>
</td>
<td width="60%">
 Reads the  record chain linked to by <i>plsnUndoNext</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsContextForward"></a><a id="clfscontextforward"></a><a id="CLFSCONTEXTFORWARD"></a><dl>
<dt><b>ClfsContextForward</b></dt>
</dl>
</td>
<td width="60%">
 Reads the record  with the LSN that immediately follows the current LSN in the read context.

</td>
</tr>
</table>
 


### -param ppvReadBuffer [out]

A pointer to a variable that receives a pointer to the target record in the log I/O block.


### -param pcbReadBuffer [out]

A pointer to  a variable that receives the size of the data that is returned in <i>*ppvReadBuffer</i>, in bytes.


### -param peRecordType [out]

A pointer to a variable that receives the  type of record read. 

This parameter is one of the <a href="https://msdn.microsoft.com/63489b1b-75de-469d-9ffc-f0353bb2fdd9">CLFS_RECORD_TYPE Constants</a>.


### -param plsnUndoNext [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure that receives the LSN of the next record in the undo record chain.


### -param plsnPrevious [out]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure that receives the LSN of the next record in the previous record chain.


### -param ppvReadContext [out]

A pointer to a variable that receives a pointer to a system-allocated read context  when a read is successful.  

If the function defers completion of an operation, it    returns a valid read-context pointer and an error status of <b>ERROR_IO_PENDING</b>.  On all other errors, the read-context pointer is <b>NULL</b>.  For more information about handling deferred completion of the function, see the Remarks section of this topic.

After obtaining all requested log records, the client must pass  the read context to <a href="https://msdn.microsoft.com/fb0a4c4e-cdb7-4c42-9102-bc76b8b70193">TerminateReadLog</a> to free the associated memory. Failure to do so results in memory leakage.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time, or passed into more than one asynchronous read at a time.</div>
<div> </div>

### -param OPTIONAL

TBD




#### - pOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure, which is required for asynchronous operation.

 This parameter can be <b>NULL</b> if asynchronous operation is not used.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following  list identifies the possible error codes.




## -remarks



The error message ERROR_LOG_BLOCK_INCOMPLETE is returned if the log block size specified by <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> is not large enough to hold a complete log block.

If <b>ReadLogRecord</b>  is called with a valid <i>pOverlapped</i> structure and the log handle is created with the overlapped option, then if a call to this function fails with an error code of <b>ERROR_IO_PENDING</b>, a pointer to a valid read context  is  placed in the variable that is pointed to by the <i>ppvReadContext</i> parameter.

If you attempt to open more read contexts than the number buffers specified in a previous call to <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a>,  ERROR_LOG_BLOCK_EXHAUSTED is returned.

To complete a log-record copy, the client should first synchronize its execution with deferred completion of the overlapped I/O operation by using  <a href="https://msdn.microsoft.com/7f999959-9b22-4491-ae2b-a2674d821110">GetOverlappedResult</a> or one of the synchronization <a href="https://msdn.microsoft.com/9c66c71d-fdfd-42ae-895c-2fc842b5bc7a">Wait Functions</a>. For more information, see <a href="https://msdn.microsoft.com/db44990e-5a0f-4153-8ff6-79dd7cda48af">Synchronization and Overlapped Input and Output</a>.

After <b>ReadLogRecord</b> completes asynchronously, the requested record  is read from the disk, but is not  resolved to a pointer in <i>*ppvReadBuffer</i>.

To complete the requested read and obtain a valid pointer to the log record, the client must call <a href="https://msdn.microsoft.com/7736106b-6c43-496e-83b8-fa433c29e680">ReadNextLogRecord</a>, which passes in the read-context pointer  that  <b>ReadLogRecord</b> returns.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time.<p class="note">CLFS read contexts should not be passed into more than one asynchronous read at a time, or the function fails with ERROR_BUSY.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff541783">CLFS_CONTEXT_MODE</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a>



<a href="https://msdn.microsoft.com/63489b1b-75de-469d-9ffc-f0353bb2fdd9">CLFS_RECORD_TYPE</a>



<a href="https://msdn.microsoft.com/a3059828-d291-493d-a4fe-13d06e49ed12">Common Log File System Functions</a>



<a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a>



<a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a>



<a href="https://msdn.microsoft.com/7736106b-6c43-496e-83b8-fa433c29e680">ReadNextLogRecord</a>



<a href="https://msdn.microsoft.com/fb0a4c4e-cdb7-4c42-9102-bc76b8b70193">TerminateReadLog</a>
 

 

