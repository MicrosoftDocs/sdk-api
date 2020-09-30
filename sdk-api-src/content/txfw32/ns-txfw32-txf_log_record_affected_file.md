---
UID: NS:txfw32._TXF_LOG_RECORD_AFFECTED_FILE
title: TXF_LOG_RECORD_AFFECTED_FILE (txfw32.h)
description: Contains information for a file that was affected by a transaction.
helpviewer_keywords: ["*PTXF_LOG_RECORD_AFFECTED_FILE","PTXF_LOG_RECORD_AFFECTED_FILE","PTXF_LOG_RECORD_AFFECTED_FILE structure pointer [Files]","TXF_LOG_RECORD_AFFECTED_FILE","TXF_LOG_RECORD_AFFECTED_FILE structure [Files]","fs.txf_log_record_affected_file","txfw32/PTXF_LOG_RECORD_AFFECTED_FILE","txfw32/TXF_LOG_RECORD_AFFECTED_FILE"]
old-location: fs\txf_log_record_affected_file.htm
tech.root: fs
ms.assetid: 9fe7375a-58ef-4807-942f-e21858f09217
ms.date: 12/05/2018
ms.keywords: '*PTXF_LOG_RECORD_AFFECTED_FILE, PTXF_LOG_RECORD_AFFECTED_FILE, PTXF_LOG_RECORD_AFFECTED_FILE structure pointer [Files], TXF_LOG_RECORD_AFFECTED_FILE, TXF_LOG_RECORD_AFFECTED_FILE structure [Files], fs.txf_log_record_affected_file, txfw32/PTXF_LOG_RECORD_AFFECTED_FILE, txfw32/TXF_LOG_RECORD_AFFECTED_FILE'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: TXF_LOG_RECORD_AFFECTED_FILE, *PTXF_LOG_RECORD_AFFECTED_FILE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TXF_LOG_RECORD_AFFECTED_FILE
 - txfw32/_TXF_LOG_RECORD_AFFECTED_FILE
 - PTXF_LOG_RECORD_AFFECTED_FILE
 - txfw32/PTXF_LOG_RECORD_AFFECTED_FILE
 - TXF_LOG_RECORD_AFFECTED_FILE
 - txfw32/TXF_LOG_RECORD_AFFECTED_FILE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - TxfW32.h
api_name:
 - TXF_LOG_RECORD_AFFECTED_FILE
---

# TXF_LOG_RECORD_AFFECTED_FILE structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Contains information for a file that was affected by a transaction.

## -struct-fields

### -field Version

The version identifier for the replication record.

### -field RecordLength

The length of this record, in bytes.

### -field Flags

This member is reserved.

### -field TxfFileId

The TxF file identifier for the file associated with this record. For more information, see <a href="/windows/desktop/api/txfw32/ns-txfw32-txf_id">TXF_ID</a>.

### -field KtmGuid

The KTM transaction GUID for this update.

### -field FileNameLength

The length of the file name, in bytes.

### -field FileNameByteOffsetInStructure

The offset of the file name from the beginning of this record.

## -see-also

<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_id">TXF_ID</a>



<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_base">TXF_LOG_RECORD_BASE</a>