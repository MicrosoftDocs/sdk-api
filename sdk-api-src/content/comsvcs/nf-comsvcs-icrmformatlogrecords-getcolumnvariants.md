---
UID: NF:comsvcs.ICrmFormatLogRecords.GetColumnVariants
title: ICrmFormatLogRecords::GetColumnVariants (comsvcs.h)
description: Formats one structured log record into an array of viewable fields.
helpviewer_keywords: ["GetColumnVariants","GetColumnVariants method [COM+]","GetColumnVariants method [COM+]","ICrmFormatLogRecords interface","ICrmFormatLogRecords interface [COM+]","GetColumnVariants method","ICrmFormatLogRecords.GetColumnVariants","ICrmFormatLogRecords::GetColumnVariants","_dtc_ICrmFormatLogRecords_GetColumnVariants","comsvcs/ICrmFormatLogRecords::GetColumnVariants","cos.icrmformatlogrecords_getcolumnvariants"]
old-location: cos\icrmformatlogrecords_getcolumnvariants.htm
tech.root: cos
ms.assetid: f2681fe3-744b-4172-8908-1d823d2e2371
ms.date: 12/05/2018
ms.keywords: GetColumnVariants, GetColumnVariants method [COM+], GetColumnVariants method [COM+],ICrmFormatLogRecords interface, ICrmFormatLogRecords interface [COM+],GetColumnVariants method, ICrmFormatLogRecords.GetColumnVariants, ICrmFormatLogRecords::GetColumnVariants, _dtc_ICrmFormatLogRecords_GetColumnVariants, comsvcs/ICrmFormatLogRecords::GetColumnVariants, cos.icrmformatlogrecords_getcolumnvariants
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
 - ICrmFormatLogRecords::GetColumnVariants
 - comsvcs/ICrmFormatLogRecords::GetColumnVariants
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
 - ICrmFormatLogRecords.GetColumnVariants
---

# ICrmFormatLogRecords::GetColumnVariants


## -description

Formats one structured log record into an array of viewable fields.

## -parameters

### -param LogRecord [in]

The structured log record to be formatted.

### -param pFormattedLogRecord [out]

A <b>Variant</b> array of the fields in this log record as <b>Variant</b> strings.

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