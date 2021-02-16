---
UID: NF:comsvcs.ICrmMonitorLogRecords.GetLogRecordVariants
title: ICrmMonitorLogRecords::GetLogRecordVariants (comsvcs.h)
description: Retrieves a structured log record given its numeric index.
helpviewer_keywords: ["GetLogRecordVariants","GetLogRecordVariants method [COM+]","GetLogRecordVariants method [COM+]","ICrmMonitorLogRecords interface","ICrmMonitorLogRecords interface [COM+]","GetLogRecordVariants method","ICrmMonitorLogRecords.GetLogRecordVariants","ICrmMonitorLogRecords::GetLogRecordVariants","_dtc_ICrmMonitorLogRecords_GetLogRecordVariants","comsvcs/ICrmMonitorLogRecords::GetLogRecordVariants","cos.icrmmonitorlogrecords_getlogrecordvariants"]
old-location: cos\icrmmonitorlogrecords_getlogrecordvariants.htm
tech.root: cos
ms.assetid: 4f020d2d-ea2d-48c2-ab79-7b412e77b39f
ms.date: 12/05/2018
ms.keywords: GetLogRecordVariants, GetLogRecordVariants method [COM+], GetLogRecordVariants method [COM+],ICrmMonitorLogRecords interface, ICrmMonitorLogRecords interface [COM+],GetLogRecordVariants method, ICrmMonitorLogRecords.GetLogRecordVariants, ICrmMonitorLogRecords::GetLogRecordVariants, _dtc_ICrmMonitorLogRecords_GetLogRecordVariants, comsvcs/ICrmMonitorLogRecords::GetLogRecordVariants, cos.icrmmonitorlogrecords_getlogrecordvariants
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICrmMonitorLogRecords::GetLogRecordVariants
 - comsvcs/ICrmMonitorLogRecords::GetLogRecordVariants
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - ComSvcs.h
api_name:
 - ICrmMonitorLogRecords.GetLogRecordVariants
---

# ICrmMonitorLogRecords::GetLogRecordVariants


## -description

Retrieves a structured log record given its numeric index.

## -parameters

### -param IndexNumber [in]

The index of the required log record.

### -param pLogRecord [out]

The log record. See <a href="/windows/desktop/api/comsvcs/nf-comsvcs-icrmcompensatorvariants-preparerecordvariants">ICrmCompensatorVariants::PrepareRecordVariants</a> for the format.

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

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmmonitorlogrecords">ICrmMonitorLogRecords</a>