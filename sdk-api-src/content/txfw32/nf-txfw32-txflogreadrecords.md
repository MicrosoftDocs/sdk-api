---
UID: NF:txfw32.TxfLogReadRecords
title: TxfLogReadRecords function (txfw32.h)
description: Reads the redo records from the log.
helpviewer_keywords: ["TxfLogReadRecords","TxfLogReadRecords function [Files]","fs.txflogreadrecords","txfw32/TxfLogReadRecords"]
old-location: fs\txflogreadrecords.htm
tech.root: fs
ms.assetid: f0f10d9c-957a-4484-bde8-337d235e3262
ms.date: 12/05/2018
ms.keywords: TxfLogReadRecords, TxfLogReadRecords function [Files], fs.txflogreadrecords, txfw32/TxfLogReadRecords
req.header: txfw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: TxfW32.lib
req.dll: TxfW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TxfLogReadRecords
 - txfw32/TxfLogReadRecords
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - TxfW32.dll
api_name:
 - TxfLogReadRecords
---

# TxfLogReadRecords function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Reads the redo records from the log.

## -parameters

### -param TxfLogContext [in]

A pointer to the context.

### -param BufferLength [in]

The size of the output buffer, in bytes.

### -param Buffer [out]

A pointer to the buffer that receives the records. For more information, see <a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_base">TXF_LOG_RECORD_BASE</a>.

### -param BytesUsed [out]

The number of bytes written to the output buffer.

### -param RecordCount [out]

The number of records written to the output buffer.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Possible error codes include the 
       following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The replication context is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Some of the available records were copied into the buffer. Call this function again to retrieve the rest 
	       of the records.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is not large enough to contain even one record. If <i>BytesUsed</i> is 
	       nonzero, then there was enough space to copy the 
	       <a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_base">TXF_LOG_RECORD_BASE</a> structure, which indicates the 
	       required buffer size to read the next complete record.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_CORRUPT</b></dt>
</dl>
</td>
<td width="60%">
The format of the log file being processed is unrecognized.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_base">TXF_LOG_RECORD_BASE</a>