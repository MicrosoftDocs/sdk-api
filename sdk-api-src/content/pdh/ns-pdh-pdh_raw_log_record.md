---
UID: NS:pdh._PDH_RAW_LOG_RECORD
title: PDH_RAW_LOG_RECORD (pdh.h)
description: The PDH_RAW_LOG_RECORD structure contains information about a binary trace log file record.
helpviewer_keywords: ["*PPDH_RAW_LOG_RECORD","PDH_LOG_TYPE_BINARY","PDH_LOG_TYPE_CSV","PDH_LOG_TYPE_PERFMON","PDH_LOG_TYPE_SQL","PDH_LOG_TYPE_TSV","PDH_RAW_LOG_RECORD","PDH_RAW_LOG_RECORD structure [Perf]","PPDH_RAW_LOG_RECORD","PPDH_RAW_LOG_RECORD structure pointer [Perf]","_win32_pdh_raw_log_record_str","base.pdh_raw_log_record_str","pdh/PDH_RAW_LOG_RECORD","pdh/PPDH_RAW_LOG_RECORD","perf.pdh_raw_log_record_str"]
old-location: perf\pdh_raw_log_record_str.htm
tech.root: perf
ms.assetid: ae96515f-ea3f-4578-a249-fb8f41cdfa69
ms.date: 12/05/2018
ms.keywords: '*PPDH_RAW_LOG_RECORD, PDH_LOG_TYPE_BINARY, PDH_LOG_TYPE_CSV, PDH_LOG_TYPE_PERFMON, PDH_LOG_TYPE_SQL, PDH_LOG_TYPE_TSV, PDH_RAW_LOG_RECORD, PDH_RAW_LOG_RECORD structure [Perf], PPDH_RAW_LOG_RECORD, PPDH_RAW_LOG_RECORD structure pointer [Perf], _win32_pdh_raw_log_record_str, base.pdh_raw_log_record_str, pdh/PDH_RAW_LOG_RECORD, pdh/PPDH_RAW_LOG_RECORD, perf.pdh_raw_log_record_str'
req.header: pdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: PDH_RAW_LOG_RECORD, *PPDH_RAW_LOG_RECORD
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _PDH_RAW_LOG_RECORD
 - pdh/_PDH_RAW_LOG_RECORD
 - PPDH_RAW_LOG_RECORD
 - pdh/PPDH_RAW_LOG_RECORD
 - PDH_RAW_LOG_RECORD
 - pdh/PDH_RAW_LOG_RECORD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Pdh.h
api_name:
 - PDH_RAW_LOG_RECORD
---

# PDH_RAW_LOG_RECORD structure


## -description

The 
<b>PDH_RAW_LOG_RECORD</b> structure contains information about a binary trace log file record.

## -struct-fields

### -field dwStructureSize

Size of this structure, in bytes. The size includes this structure and the <b>RawBytes</b> appended to the end of this structure.

### -field dwRecordType

Type of record. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_BINARY"></a><a id="pdh_log_type_binary"></a><dl>
<dt><b>PDH_LOG_TYPE_BINARY</b></dt>
</dl>
</td>
<td width="60%">
A binary trace format record

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_CSV"></a><a id="pdh_log_type_csv"></a><dl>
<dt><b>PDH_LOG_TYPE_CSV</b></dt>
</dl>
</td>
<td width="60%">
A comma-separated-value format record

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_PERFMON"></a><a id="pdh_log_type_perfmon"></a><dl>
<dt><b>PDH_LOG_TYPE_PERFMON</b></dt>
</dl>
</td>
<td width="60%">
A Perfmon format record

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_SQL"></a><a id="pdh_log_type_sql"></a><dl>
<dt><b>PDH_LOG_TYPE_SQL</b></dt>
</dl>
</td>
<td width="60%">
A SQL format record

</td>
</tr>
<tr>
<td width="40%"><a id="PDH_LOG_TYPE_TSV"></a><a id="pdh_log_type_tsv"></a><dl>
<dt><b>PDH_LOG_TYPE_TSV</b></dt>
</dl>
</td>
<td width="60%">
A tab-separated-value format record

</td>
</tr>
</table>

### -field dwItems

Size of the <b>RawBytes</b> data.

### -field RawBytes

Binary record.

## -see-also

<a href="/windows/desktop/api/pdh/nf-pdh-pdhreadrawlogrecord">PdhReadRawLogRecord</a>