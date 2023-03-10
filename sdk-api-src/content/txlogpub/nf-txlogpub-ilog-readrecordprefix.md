---
UID: NF:txlogpub.ILog.ReadRecordPrefix
title: ILog::ReadRecordPrefix (txlogpub.h)
description: Reads an initial part of a record from the log.
helpviewer_keywords: ["ILog interface [COM]","ReadRecordPrefix method","ILog.ReadRecordPrefix","ILog::ReadRecordPrefix","ReadRecordPrefix","ReadRecordPrefix method [COM]","ReadRecordPrefix method [COM]","ILog interface","_com_ilog_readrecordprefix","com.ilog_readrecordprefix","txlogpub/ILog::ReadRecordPrefix"]
old-location: com\ilog_readrecordprefix.htm
tech.root: com
ms.assetid: 4a2b8529-b342-4491-a7ce-db4150223682
ms.date: 12/05/2018
ms.keywords: ILog interface [COM],ReadRecordPrefix method, ILog.ReadRecordPrefix, ILog::ReadRecordPrefix, ReadRecordPrefix, ReadRecordPrefix method [COM], ReadRecordPrefix method [COM],ILog interface, _com_ilog_readrecordprefix, com.ilog_readrecordprefix, txlogpub/ILog::ReadRecordPrefix
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
 - ILog::ReadRecordPrefix
 - txlogpub/ILog::ReadRecordPrefix
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
 - ILog.ReadRecordPrefix
---

# ILog::ReadRecordPrefix


## -description

Reads an initial part of a record from the log.

## -parameters

### -param lsnToRead [in]

The LSN of the record to be read.

### -param plsnPrev [in, out]

A pointer to the LSN of the previous record (the record immediately preceding the record to read). You may pass <b>NULL</b> if the LSN of the previous record is not needed. This parameter is 0 if there is no previous record in the log or if an error occurs.

### -param plsnNext [in, out]

A pointer to the LSN of the next record (the record immediately following the record to read). You may pass <b>NULL</b> if the LSN of the next record is not needed. This parameter is MAXLSN (0x7FFFFFFFFFFFFFFF) if there is no next record in the log. This parameter is 0 if an error occurs.

### -param pbData [out]

A pointer to a buffer into which the record data is to be read.

### -param pcbData [in, out]

A pointer to a variable that contains the size in bytes of the buffer on input, and will contain the size in bytes of the record data read on return.

### -param pcbRecord [out]

A pointer to a variable that will contain the size in bytes of the entire record on return. You may pass <b>NULL</b> if the size of the entire record is not needed.

## -returns

This method can return the following values, as well as other <b>HRESULT</b> values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The record was successfully read from the log.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_INVALIDLSN</b></dt>
</dl>
</td>
<td width="60%">
<i>lsnToRead</i> is outside of the current limits of the log. See <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-getloglimits">ILog::GetLogLimits</a>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>lsnToRead</i> is within the current limits of the log, but it is not the LSN of a record in the log.

</td>
</tr>
</table>

## -remarks

Although records appended to the log using <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-appendrecord">ILog::AppendRecord</a> may be concatenated from multiple BLOBs, <b>ReadRecordPrefix</b> returns the record as a single opaque blob of data. <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a> provides no method to extract individual BLOBs from the record. It is the responsibility of the caller to parse the data in records returned by <b>ReadRecordPrefix</b>.

## -see-also

<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>