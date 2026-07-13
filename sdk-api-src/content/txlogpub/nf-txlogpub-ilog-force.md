---
UID: NF:txlogpub.ILog.Force
title: ILog::Force (txlogpub.h)
description: Forces the contents of the log to disk, at least up through the specified LSN.
helpviewer_keywords: ["Force","Force method [COM]","Force method [COM]","ILog interface","ILog interface [COM]","Force method","ILog.Force","ILog::Force","_com_ilog_force","com.ilog_force","txlogpub/ILog::Force"]
old-location: com\ilog_force.htm
tech.root: com
ms.assetid: 91df6049-37ce-4a46-b401-9af7d9c09f14
ms.date: 12/05/2018
ms.keywords: Force, Force method [COM], Force method [COM],ILog interface, ILog interface [COM],Force method, ILog.Force, ILog::Force, _com_ilog_force, com.ilog_force, txlogpub/ILog::Force
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
 - ILog::Force
 - txlogpub/ILog::Force
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
 - ILog.Force
---

# ILog::Force


## -description

Forces the contents of the log to disk, at least up through the specified LSN.

## -parameters

### -param lsnMinToForce [in]

At the very least, all records that have not yet been written to disk with an LSN less than or equal to <i>lsnMinToForce</i> must be written to disk now. An implementation may, however, choose to write more records than what is strictly required. For example, an implementation is allowed to force all records to disk, regardless of the value of <i>lsnMinToForce</i>. Passing 0 as <i>lsnMinToForce</i> indicates that the entire log is to be forced to disk.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The log may also be forced to disk after appending individual records. See <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-appendrecord">ILog::AppendRecord</a>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
A failure return value indicates that any records appended to the log since the last time it was successfully forced are not guaranteed to be on disk. The <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a> interface does not provide a method to determine which records have been successfully written to disk. If you need to know which records were successfully written to disk, you must force the log for each record. See <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-appendrecord">ILog::AppendRecord</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
It is recommended that you flush file buffers (for example, using the <a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a> function) before returning from this method.

## -see-also

<a href="/windows/desktop/api/fileapi/nf-fileapi-flushfilebuffers">FlushFileBuffers</a>



<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>