---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _PDH_RAW_LOG_RECORD structure


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




<a href="https://msdn.microsoft.com/fb93b6ea-ca31-4ff1-a553-b02388be8b72">PdhReadRawLogRecord</a>
 

 

