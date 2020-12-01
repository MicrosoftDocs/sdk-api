---
UID: NF:clfsw32.ReadNextLogRecord
title: ReadNextLogRecord function (clfsw32.h)
description: Reads the next record in a sequence that is initiated by a call to ReadLogRecord or ReadLogRestartArea.
helpviewer_keywords: ["ClfsClientRecord","ClfsDataRecord","ClfsRestartRecord","ReadNextLogRecord","ReadNextLogRecord function [Files]","clfsw32/ReadNextLogRecord","fs.readnextlogrecord"]
old-location: fs\readnextlogrecord.htm
tech.root: fs
ms.assetid: 7736106b-6c43-496e-83b8-fa433c29e680
ms.date: 12/05/2018
ms.keywords: ClfsClientRecord, ClfsDataRecord, ClfsRestartRecord, ReadNextLogRecord, ReadNextLogRecord function [Files], clfsw32/ReadNextLogRecord, fs.readnextlogrecord
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
 - ReadNextLogRecord
 - clfsw32/ReadNextLogRecord
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
 - ReadNextLogRecord
---

# ReadNextLogRecord function


## -description

Reads the next record in a sequence that is initiated by a call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a> or <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a>.   By using <b>ReadNextLogRecord</b> iteratively, a client can read all records of a specified type in a log.  The direction of enumeration is determined by specifying the context mode when beginning the read sequence.

## -parameters

### -param pvReadContext [in, out]

A pointer to a  read context  that the system allocates and creates during a successful call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a> or <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a>.  

If the function defers completion of an operation, it  returns a pointer to a valid read context and an error status of <b>ERROR_IO_PENDING</b>.  For information about handling asynchronous completion, see the Remarks section of this topic.

### -param ppvBuffer [out]

A pointer to a variable that receives a pointer to the read data.

### -param pcbBuffer [out]

A pointer to a variable that receives the size of the read data that is returned in <i>ppvReadBuffer</i>, in bytes.

### -param peRecordType [in, out]

A pointer that, on input, specifies   the record type filter of the next record read, and on output specifies the record type that is returned.    

Clients can specify any of the following record types.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ClfsDataRecord"></a><a id="clfsdatarecord"></a><a id="CLFSDATARECORD"></a><dl>
<dt><b>ClfsDataRecord</b></dt>
</dl>
</td>
<td width="60%">
 Only user-data records are read.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsRestartRecord"></a><a id="clfsrestartrecord"></a><a id="CLFSRESTARTRECORD"></a><dl>
<dt><b>ClfsRestartRecord</b></dt>
</dl>
</td>
<td width="60%">
 Only restart records are read.

</td>
</tr>
<tr>
<td width="40%"><a id="ClfsClientRecord"></a><a id="clfsclientrecord"></a><a id="CLFSCLIENTRECORD"></a><dl>
<dt><b>ClfsClientRecord</b></dt>
</dl>
</td>
<td width="60%">
 All restart and data records are read.

</td>
</tr>
</table>

### -param plsnUser [in, optional]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that specifies   the log client  to read this log sequence number (LSN) as the next LSN instead of  reading forward to the next record, reading the previous LSN, or reading the next undo LSN.  

This parameter gives log clients the ability to cursor through user-defined LSN chains in client buffers.  The relationship of this parameter to the current LSN held by the read context must be consistent with the context mode, <i>ecxMode</i>,  that is specified in the <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a>  entry points; otherwise, an error code of <b>ERROR_INVALID_PARAMETER</b> is returned.

### -param plsnUndoNext [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that receives the LSN of the next record in an undo record chain.

### -param plsnPrevious [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that receives the LSN of the next record in the previous record chain.

### -param plsnRecord [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that receives the LSN of the current record read into the read context.

### -param pOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that is required for asynchronous operation. 

This parameter can be <b>NULL</b> if asynchronous operation is not used.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. 

The following  list identifies the  possible error codes:

## -remarks

If <b>ReadNextLogRecord</b>  returns with a status code of <b>ERROR_IO_PENDING</b>, the client should synchronize its execution with deferred completion of the overlapped I/O operation by using <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a>, or one of the synchronization <a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>. For more information, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>. 

After <b>ReadNextLogRecord</b> completes asynchronously, the requested record  is  read from the disk, but is not   resolved to a pointer in <i>*ppvReadBuffer</i>. To obtain a valid pointer to the record,  the client must call <b>ReadNextLogRecord</b> a second time.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time.<p class="note">CLFS read contexts should not be passed into more than one asynchronous read at a time, or the function fails with ERROR_READ.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/clfs-record-type-constants">CLFS_RECORD_TYPE</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrecord">ReadLogRecord</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a>



<a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>