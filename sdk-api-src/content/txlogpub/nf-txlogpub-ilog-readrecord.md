---
UID: NF:txlogpub.ILog.ReadRecord
title: ILog::ReadRecord (txlogpub.h)
description: Read a record from the log.
helpviewer_keywords: ["ILog interface [COM]","ReadRecord method","ILog.ReadRecord","ILog::ReadRecord","ReadRecord","ReadRecord method [COM]","ReadRecord method [COM]","ILog interface","_com_ilog_readrecord","com.ilog_readrecord","txlogpub/ILog::ReadRecord"]
old-location: com\ilog_readrecord.htm
tech.root: com
ms.assetid: 756d56a4-083f-45cd-bcdc-7c8a15dabae6
ms.date: 12/05/2018
ms.keywords: ILog interface [COM],ReadRecord method, ILog.ReadRecord, ILog::ReadRecord, ReadRecord, ReadRecord method [COM], ReadRecord method [COM],ILog interface, _com_ilog_readrecord, com.ilog_readrecord, txlogpub/ILog::ReadRecord
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
 - ILog::ReadRecord
 - txlogpub/ILog::ReadRecord
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
 - ILog.ReadRecord
---

# ILog::ReadRecord


## -description

Read a record from the log.

## -parameters

### -param lsnToRead [in]

The LSN of the record to be read.

### -param plsnPrev [in, out]

A pointer to the LSN of the previous record (the record immediately preceding the record to be read). This parameter can be <b>NULL</b> if the LSN of the previous record is not needed. This parameter is 0 if there is no previous record in the log, or if an error occurs.

### -param plsnNext [in, out]

A pointer to the LSN of the next record (the record immediately following the record to read). This parameter can be <b>NULL</b> if the LSN of the next record is not needed. This parameter is MAXLSN (0x7FFFFFFFFFFFFFFF) if there is no next record in the log. This parameter is 0 if an error occurs.

### -param ppbData [out]

A pointer to a variable that will contain a pointer to the record data on return. The memory for this data is allocated by <b>ReadRecord</b> and freed by the caller (see <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>). This parameter is <b>NULL</b> if an error occurs.

### -param pcbData [out]

A pointer to a variable that receives the size of the record data, in bytes, on return.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The record was not returned due to a lack of memory.

</td>
</tr>
</table>

## -remarks

Although records appended to the log using <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-appendrecord">ILog::AppendRecord</a> may be concatenated from multiple BLOBs, <b>ReadRecord</b> returns the record as a single opaque blob of data. <a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a> provides no method to extract individual BLOBs from the record. It is the responsibility of the caller to parse the data in records returned by <b>ReadRecord</b>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If the log contains very large records, this method may fail because <b>ReadRecord</b> was unable to allocate sufficient memory for the record data. If the size of records is bounded or if you only need an initial part of the record, it may be more efficient to call <a href="/windows/desktop/api/txlogpub/nf-txlogpub-ilog-readrecordprefix">ILog::ReadRecordPrefix</a>.

## -see-also

<a href="/windows/desktop/api/txlogpub/nn-txlogpub-ilog">ILog</a>