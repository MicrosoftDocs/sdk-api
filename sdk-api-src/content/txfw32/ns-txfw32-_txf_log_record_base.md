---
UID: NS:txfw32._TXF_LOG_RECORD_BASE
title: "_TXF_LOG_RECORD_BASE"
author: windows-sdk-content
description: Contains the basic record information.
old-location: fs\txf_log_record_base.htm
old-project: FileIO
ms.assetid: b891f763-13dd-4b40-aff3-3fccb693d76a
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: "*PTXF_LOG_RECORD_BASE, PTXF_LOG_RECORD_BASE, PTXF_LOG_RECORD_BASE structure pointer [Files], TXF_LOG_RECORD_BASE, TXF_LOG_RECORD_BASE structure [Files], TXF_LOG_RECORD_TYPE_AFFECTED_FILE, TXF_LOG_RECORD_TYPE_TRUNCATE, TXF_LOG_RECORD_TYPE_WRITE, _TXF_LOG_RECORD_BASE, fs.txf_log_record_base, txfw32/PTXF_LOG_RECORD_BASE, txfw32/TXF_LOG_RECORD_BASE"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: TXF_LOG_RECORD_BASE, *PTXF_LOG_RECORD_BASE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TxfW32.h
api_name:
 - TXF_LOG_RECORD_BASE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# _TXF_LOG_RECORD_BASE structure


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Contains the basic record information.


## -struct-fields




### -field Version

The version identifier for the replication record.


### -field RecordType

The record type. This member can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXF_LOG_RECORD_TYPE_AFFECTED_FILE"></a><a id="txf_log_record_type_affected_file"></a><dl>
<dt><b>TXF_LOG_RECORD_TYPE_AFFECTED_FILE</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The record is a <a href="https://msdn.microsoft.com/9fe7375a-58ef-4807-942f-e21858f09217">TXF_LOG_RECORD_AFFECTED_FILE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TXF_LOG_RECORD_TYPE_TRUNCATE"></a><a id="txf_log_record_type_truncate"></a><dl>
<dt><b>TXF_LOG_RECORD_TYPE_TRUNCATE</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The record is a <a href="https://msdn.microsoft.com/9b6e9be5-39e7-47e3-846f-ea2e5e04597f">TXF_LOG_RECORD_TRUNCATE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="TXF_LOG_RECORD_TYPE_WRITE"></a><a id="txf_log_record_type_write"></a><dl>
<dt><b>TXF_LOG_RECORD_TYPE_WRITE</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The record is a <a href="https://msdn.microsoft.com/754ea93e-bc82-498e-8333-eda3262aebc0">TXF_LOG_RECORD_WRITE</a> structure.

</td>
</tr>
</table>
 


### -field RecordLength

The length of this record, in bytes.


## -see-also




<a href="https://msdn.microsoft.com/9fe7375a-58ef-4807-942f-e21858f09217">TXF_LOG_RECORD_AFFECTED_FILE</a>



<a href="https://msdn.microsoft.com/9b6e9be5-39e7-47e3-846f-ea2e5e04597f">TXF_LOG_RECORD_TRUNCATE</a>



<a href="https://msdn.microsoft.com/754ea93e-bc82-498e-8333-eda3262aebc0">TXF_LOG_RECORD_WRITE</a>



<a href="https://msdn.microsoft.com/f0f10d9c-957a-4484-bde8-337d235e3262">TxfLogReadRecords</a>
 

 

