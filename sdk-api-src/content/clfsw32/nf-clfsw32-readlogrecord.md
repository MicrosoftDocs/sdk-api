---
UID: NF:clfsw32.ReadLogRecord
title: ReadLogRecord function (clfsw32.h)
description: Initiates a sequence of reads from a specified log sequence number (LSN) in one of three modes, and returns the first of the specified log records and a read context.
helpviewer_keywords: ["ClfsContextForward","ClfsContextPrevious","ClfsContextUndoNext","ReadLogRecord","ReadLogRecord function [Files]","clfsw32/ReadLogRecord","fs.readlogrecord"]
old-location: fs\readlogrecord.htm
tech.root: fs
ms.assetid: 1c56c47b-d898-4c70-ba70-8978057c66b9
ms.date: 12/05/2018
ms.keywords: ClfsContextForward, ClfsContextPrevious, ClfsContextUndoNext, ReadLogRecord, ReadLogRecord function [Files], clfsw32/ReadLogRecord, fs.readlogrecord
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ReadLogRecord
 - clfsw32/ReadLogRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - ReadLogRecord
---

# ReadLogRecord function


## -description

Initiates a sequence of reads from a specified log sequence number (LSN) in one of three modes, and returns the first of the specified log records and a read context.  A client can read subsequent records in the designated mode by passing the read context to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readnextlogrecord">ReadNextLogRecord</a>.

## -parameters

### -param pvMarshal [in]

A pointer to a  marshaling context that is allocated by using the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> function.

### -param plsnFirst [in]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies the log sequence number (LSN) of the record  where  the read operation should start.  

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

This parameter is one of the <a href="/previous-versions/windows/desktop/clfs/clfs-record-type-constants">CLFS_RECORD_TYPE Constants</a>.

### -param plsnUndoNext [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that receives the LSN of the next record in the undo record chain.

### -param plsnPrevious [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that receives the LSN of the next record in the previous record chain.

### -param ppvReadContext [out]

A pointer to a variable that receives a pointer to a system-allocated read context  when a read is successful.  

If the function defers completion of an operation, it    returns a valid read-context pointer and an error status of <b>ERROR_IO_PENDING</b>.  On all other errors, the read-context pointer is <b>NULL</b>.  For more information about handling deferred completion of the function, see the Remarks section of this topic.

After obtaining all requested log records, the client must pass  the read context to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatereadlog">TerminateReadLog</a> to free the associated memory. Failure to do so results in memory leakage.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time, or passed into more than one asynchronous read at a time.</div>
<div> </div>

### -param pOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure, which is required for asynchronous operation.

 This parameter can be <b>NULL</b> if asynchronous operation is not used.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following  list identifies the possible error codes.

## -remarks

The error message ERROR_LOG_BLOCK_INCOMPLETE is returned if the log block size specified by <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> is not large enough to hold a complete log block.

If <b>ReadLogRecord</b>  is called with a valid <i>pOverlapped</i> structure and the log handle is created with the overlapped option, then if a call to this function fails with an error code of <b>ERROR_IO_PENDING</b>, a pointer to a valid read context  is  placed in the variable that is pointed to by the <i>ppvReadContext</i> parameter.

If you attempt to open more read contexts than the number buffers specified in a previous call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a>,  ERROR_LOG_BLOCK_EXHAUSTED is returned.

To complete a log-record copy, the client should first synchronize its execution with deferred completion of the overlapped I/O operation by using  <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or one of the synchronization <a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>. For more information, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

After <b>ReadLogRecord</b> completes asynchronously, the requested record  is read from the disk, but is not  resolved to a pointer in <i>*ppvReadBuffer</i>.

To complete the requested read and obtain a valid pointer to the log record, the client must call <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readnextlogrecord">ReadNextLogRecord</a>, which passes in the read-context pointer  that  <b>ReadLogRecord</b> returns.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time.<p class="note">CLFS read contexts should not be passed into more than one asynchronous read at a time, or the function fails with ERROR_BUSY.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/clfs/ne-clfs-clfs_context_mode">CLFS_CONTEXT_MODE</a>



<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/clfs-record-type-constants">CLFS_RECORD_TYPE</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readnextlogrecord">ReadNextLogRecord</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-terminatereadlog">TerminateReadLog</a>