---
UID: NF:clfsw32.ReadPreviousLogRestartArea
title: ReadPreviousLogRestartArea function (clfsw32.h)
description: Reads the previous log restart area that is relative to the current restart record specified in the read context, pvReadContext. This read context is the one previously created by a call to ReadLogRestartArea.
helpviewer_keywords: ["ReadPreviousLogRestartArea","ReadPreviousLogRestartArea function [Files]","clfsw32/ReadPreviousLogRestartArea","fs.readpreviouslogrestartarea"]
old-location: fs\readpreviouslogrestartarea.htm
tech.root: fs
ms.assetid: f304dbb7-7d5c-403c-9418-60947cc4c3a1
ms.date: 12/05/2018
ms.keywords: ReadPreviousLogRestartArea, ReadPreviousLogRestartArea function [Files], clfsw32/ReadPreviousLogRestartArea, fs.readpreviouslogrestartarea
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
 - ReadPreviousLogRestartArea
 - clfsw32/ReadPreviousLogRestartArea
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
 - ReadPreviousLogRestartArea
---

# ReadPreviousLogRestartArea function


## -description

Reads the previous log restart area that is relative to the current restart record specified in the read context, <i>pvReadContext</i>. This read context is the one previously created by  a call to <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a>.

## -parameters

### -param pvReadContext [in]

A pointer to a system-allocated read context that <a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a> returns.

  Even when those functions return <b>ERROR_IO_PENDING</b>, they still return a pointer to a valid read context. For information about  asynchronous completion, see the Remarks section of this topic.

### -param ppvRestartBuffer [out]

A pointer to a variable that receives a pointer to the restart data.

### -param pcbRestartBuffer [out]

A pointer to a variable that receives the size of the restart data at <i>*ppvRestartBuffer</i>, in bytes.

### -param plsnRestart [out]

A pointer to a <a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a> structure that receives the log sequence number (LSN) of the restart area  that   this function returns.

### -param pOverlapped [in, out, optional]

A pointer to an <a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a> structure that  is required for asynchronous operation. 

This parameter can be <b>NULL</b> if asynchronous operation is not used.

## -returns

If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The following list identifies the possible error codes:

## -remarks

The error message ERROR_LOG_BLOCK_INCOMPLETE is returned if the log block size specified by <a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogmarshallingarea">CreateLogMarshallingArea</a> is not large enough to hold a complete log block.

If <b>ReadPreviousLogRestartArea</b>  fails with an error code of <b>ERROR_IO_PENDING</b>, a pointer to a valid read context  is placed in the variable that is pointed to by the <i>ppvReadContext</i> parameter.

To complete the log-record copy, the client should first synchronize its execution with deferred completion of the overlapped I/O operation by using <a href="/windows/desktop/api/ioapiset/nf-ioapiset-getoverlappedresult">GetOverlappedResult</a> or one of the synchronization <a href="/windows/desktop/Sync/wait-functions">Wait Functions</a>. For more information, see <a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>.

After <b>ReadPreviousLogRestartArea</b> completes asynchronously, the requested restart area is read from the disk, but a valid pointer to it is not  placed in <i>*ppvRestartBuffer</i>.

To obtain a valid pointer,  the client must call <b>ReadPreviousLogRestartArea</b> a second time.

<div class="alert"><b>Note</b>  Common Log File System (CLFS) read contexts are not thread-safe. They should not be used by more than one thread at a time.<p class="note">CLFS read contexts should not be passed into more than one asynchronous read at a time, or the function fails with ERROR_READ.

</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/clfs/ns-clfs-cls_lsn">CLFS_LSN</a>



<a href="/previous-versions/windows/desktop/clfs/common-log-file-system-functions">Common Log File System Functions</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-createlogfile">CreateLogFile</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-overlapped">OVERLAPPED</a>



<a href="/windows/desktop/api/clfsw32/nf-clfsw32-readlogrestartarea">ReadLogRestartArea</a>



<a href="/windows/desktop/Sync/synchronization-and-overlapped-input-and-output">Synchronization and Overlapped Input and Output</a>