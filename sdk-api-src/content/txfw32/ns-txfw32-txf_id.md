---
UID: NS:txfw32._TXF_ID
title: TXF_ID (txfw32.h)
description: Represents a unique identifier within the context of the Resource Manager.
helpviewer_keywords: ["*PTXF_ID","PTXF_ID","PTXF_ID structure pointer [Files]","TXF_ID","TXF_ID structure [Files]","fs.txf_id","txfw32/PTXF_ID","txfw32/TXF_ID"]
old-location: fs\txf_id.htm
tech.root: fs
ms.assetid: b7bdb226-69ce-4226-b826-baf9c732ec52
ms.date: 12/05/2018
ms.keywords: '*PTXF_ID, PTXF_ID, PTXF_ID structure pointer [Files], TXF_ID, TXF_ID structure [Files], fs.txf_id, txfw32/PTXF_ID, txfw32/TXF_ID'
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
req.typenames: TXF_ID, *PTXF_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _TXF_ID
 - txfw32/_TXF_ID
 - PTXF_ID
 - txfw32/PTXF_ID
 - TXF_ID
 - txfw32/TXF_ID
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
 - TXF_ID
---

# TXF_ID structure


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Represents a unique identifier within the context of the Resource Manager.

## -struct-fields

### -field LowPart

The low part of the identifier.

### -field HighPart

The high part of the identifier.

## -see-also

<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_affected_file">TXF_LOG_RECORD_AFFECTED_FILE</a>



<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_base">TXF_LOG_RECORD_BASE</a>



<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_truncate">TXF_LOG_RECORD_TRUNCATE</a>



<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_log_record_write">TXF_LOG_RECORD_WRITE</a>



<a href="/windows/desktop/api/txfw32/nf-txfw32-txflogcreatefilereadcontext">TxfLogCreateFileReadContext</a>