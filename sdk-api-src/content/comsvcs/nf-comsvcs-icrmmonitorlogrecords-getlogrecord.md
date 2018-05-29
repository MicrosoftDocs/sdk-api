---
UID: NF:comsvcs.ICrmMonitorLogRecords.GetLogRecord
title: ICrmMonitorLogRecords::GetLogRecord
author: windows-sdk-content
description: Retrieves an unstructured log record given its numeric index.
old-location: cos\icrmmonitorlogrecords_getlogrecord.htm
old-project: cossdk
ms.assetid: 9b5b566a-e98c-482d-9959-3498000875d3
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: GetLogRecord, GetLogRecord method [COM+], GetLogRecord method [COM+],ICrmMonitorLogRecords interface, ICrmMonitorLogRecords interface [COM+],GetLogRecord method, ICrmMonitorLogRecords.GetLogRecord, ICrmMonitorLogRecords::GetLogRecord, _dtc_ICrmMonitorLogRecords_GetLogRecord, comsvcs/ICrmMonitorLogRecords::GetLogRecord, cos.icrmmonitorlogrecords_getlogrecord
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: TRACKING_COLL_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComSvcs.h
api_name:
-	ICrmMonitorLogRecords.GetLogRecord
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICrmMonitorLogRecords::GetLogRecord


## -description


Retrieves an unstructured log record given its numeric index.


## -parameters




### -param dwIndex [in]

The index of the required log record.


### -param pCrmLogRec [in, out]

The log record, as a <a href="https://msdn.microsoft.com/0af0eba5-6e8c-4b1d-aec4-f9a1ffe7bce6">CrmLogRecordRead</a> structure.


## -returns



This method can return the following values.

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
The method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A <b>NULL</b> pointer was provided as an argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The index is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_WRONGSTATE</b></dt>
</dl>
</td>
<td width="60%">
Attempting to read unstructured records but written records are structured.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>XACT_E_TRANSACTIONCLOSED</b></dt>
</dl>
</td>
<td width="60%">
The transaction has completed, and the log records have been discarded from the log file. They are no longer available.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5077ad2a-89c1-43f7-a7e0-7bd8036147b6">ICrmMonitorLogRecords</a>
 

 

