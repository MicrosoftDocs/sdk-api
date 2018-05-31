---
UID: NF:txlogpub.ILog.ReadRecord
title: ILog::ReadRecord
author: windows-sdk-content
description: Read a record from the log.
old-location: com\ilog_readrecord.htm
old-project: com
ms.assetid: 756d56a4-083f-45cd-bcdc-7c8a15dabae6
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: ILog interface [COM],ReadRecord method, ILog.ReadRecord, ILog::ReadRecord, ReadRecord, ReadRecord method [COM], ReadRecord method [COM],ILog interface, _com_ilog_readrecord, com.ilog_readrecord, txlogpub/ILog::ReadRecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
req.typenames: RECORD_READING_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Txlogpub.h
api_name:
-	ILog.ReadRecord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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

A pointer to a variable that will contain a pointer to the record data on return. The memory for this data is allocated by <b>ReadRecord</b> and freed by the caller (see <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>). This parameter is <b>NULL</b> if an error occurs.


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
<i>lsnToRead</i> is outside of the current limits of the log. See <a href="https://msdn.microsoft.com/06238436-6807-4588-9af9-03eb4c12f4e1">ILog::GetLogLimits</a>.

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



Although records appended to the log using <a href="https://msdn.microsoft.com/e739acb5-4d93-4871-8b35-54d45138fe0f">ILog::AppendRecord</a> may be concatenated from multiple BLOBs, <b>ReadRecord</b> returns the record as a single opaque blob of data. <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> provides no method to extract individual BLOBs from the record. It is the responsibility of the caller to parse the data in records returned by <b>ReadRecord</b>.

<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
If the log contains very large records, this method may fail because <b>ReadRecord</b> was unable to allocate sufficient memory for the record data. If the size of records is bounded or if you only need an initial part of the record, it may be more efficient to call <a href="https://msdn.microsoft.com/4a2b8529-b342-4491-a7ce-db4150223682">ILog::ReadRecordPrefix</a>.




## -see-also




<a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a>
 

 

