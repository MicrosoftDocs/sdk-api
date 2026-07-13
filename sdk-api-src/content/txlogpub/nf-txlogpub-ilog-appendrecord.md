---
UID: NF:txlogpub.ILog.AppendRecord
title: ILog::AppendRecord (txlogpub.h)
description: Write a new record to the end of the log.
helpviewer_keywords: ["AppendRecord","AppendRecord method [COM]","AppendRecord method [COM]","ILog interface","ILog interface [COM]","AppendRecord method","ILog.AppendRecord","ILog::AppendRecord","_com_ilog_appendrecord","com.ilog_appendrecord","txlogpub/ILog::AppendRecord"]
old-location: com\ilog_appendrecord.htm
tech.root: com
ms.assetid: e739acb5-4d93-4871-8b35-54d45138fe0f
ms.date: 12/05/2018
ms.keywords: AppendRecord, AppendRecord method [COM], AppendRecord method [COM],ILog interface, ILog interface [COM],AppendRecord method, ILog.AppendRecord, ILog::AppendRecord, _com_ilog_appendrecord, com.ilog_appendrecord, txlogpub/ILog::AppendRecord
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ILog::AppendRecord
 - txlogpub/ILog::AppendRecord
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Txlogpub.h
api_name:
 - ILog.AppendRecord
---

# ILog::AppendRecord


## -description

Write a new record to the end of the log.

## -parameters

### -param rgBlob [in]

A pointer to an array of BLOBs of data to be written.

### -param cBlob [in]

The size of the <i>rgBlob</i> array, in elements.

### -param fForceNow [in]

Indicates whether to force the data to disk. If <b>TRUE</b>, the contents of the log up to this record must be forced to disk before the call returns. If <b>FALSE</b>, this record may be buffered in memory to be written after the call returns successfully.

### -param plsn [in, out]

A pointer to the LSN of the newly appended record. If the LSN of the newly appended record is not needed, this parameter can be <b>NULL</b>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Each log record written or read by <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a> is an opaque BLOB of data. As a convenience to callers, <b>AppendRecord</b> allows multiple BLOBs to be concatenated into a single record; because many implementations of <b>ILog</b> will copy records to a buffer in memory, it may be inefficient for the caller to allocate memory for concatenating the parts of a record. However, once a record is appended to the log, <b>ILog</b> provides no method to extract individual BLOBs from the record. It is the responsibility of the caller to parse the data in records read from the log. See <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-readrecord">ILog::ReadRecord</a>.


<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A failure return value indicates that any records appended to the log since the last time it was successfully forced are not guaranteed to be on disk. The <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a> interface does not provide a method to determine which records have been successfully written to disk. If you need to know which records were successfully written to disk, you must force the log for each record.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If <i>fForceNow</i> is <b>TRUE</b>, it is recommended that you flush file buffers (for example, using the <a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> function) before returning from this method.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a>



<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>