---
UID: NF:comsvcs.ICrmFormatLogRecords.GetColumn
title: ICrmFormatLogRecords::GetColumn (comsvcs.h)
description: Formats one unstructured log record into an array of viewable fields.
helpviewer_keywords: ["GetColumn","GetColumn method [COM+]","GetColumn method [COM+]","ICrmFormatLogRecords interface","ICrmFormatLogRecords interface [COM+]","GetColumn method","ICrmFormatLogRecords.GetColumn","ICrmFormatLogRecords::GetColumn","_dtc_ICrmFormatLogRecords_GetColumn","comsvcs/ICrmFormatLogRecords::GetColumn","cos.icrmformatlogrecords_getcolumn"]
old-location: cos\icrmformatlogrecords_getcolumn.htm
tech.root: cos
ms.assetid: 5234f582-88e2-4a9a-8650-d0d2d4b39f31
ms.date: 12/05/2018
ms.keywords: GetColumn, GetColumn method [COM+], GetColumn method [COM+],ICrmFormatLogRecords interface, ICrmFormatLogRecords interface [COM+],GetColumn method, ICrmFormatLogRecords.GetColumn, ICrmFormatLogRecords::GetColumn, _dtc_ICrmFormatLogRecords_GetColumn, comsvcs/ICrmFormatLogRecords::GetColumn, cos.icrmformatlogrecords_getcolumn
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
 - ICrmFormatLogRecords::GetColumn
 - comsvcs/ICrmFormatLogRecords::GetColumn
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
 - ICrmFormatLogRecords.GetColumn
---

# ICrmFormatLogRecords::GetColumn


## -description

Formats one unstructured log record into an array of viewable fields.

## -parameters

### -param CrmLogRec [in]

The unstructured log record to be formatted, as a <a href="/windows/desktop/api/comsvcs/ns-comsvcs-crmlogrecordread">CrmLogRecordRead</a> structure.

### -param pFormattedLogRecord [out]

The formatted log record, as a <b>Variant</b> array of the fields in this log record as <b>Variant</b> strings.

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
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
The log record could not be formatted.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/comsvcs/nn-comsvcs-icrmformatlogrecords">ICrmFormatLogRecords</a>