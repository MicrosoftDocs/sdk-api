---
UID: NF:txfw32.TxfLogCreateFileReadContext
title: TxfLogCreateFileReadContext function (txfw32.h)
description: Creates a context to be used to read replication records.
helpviewer_keywords: ["TxfLogCreateFileReadContext","TxfLogCreateFileReadContext function [Files]","fs.txflogcreatefilereadcontext","txfw32/TxfLogCreateFileReadContext"]
old-location: fs\txflogcreatefilereadcontext.htm
tech.root: fs
ms.assetid: 57218f53-adcd-4a9a-b772-d3dab576b8c1
ms.date: 12/05/2018
ms.keywords: TxfLogCreateFileReadContext, TxfLogCreateFileReadContext function [Files], fs.txflogcreatefilereadcontext, txfw32/TxfLogCreateFileReadContext
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
req.lib: TxfW32.lib
req.dll: TxfW32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TxfLogCreateFileReadContext
 - txfw32/TxfLogCreateFileReadContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - TxfW32.dll
api_name:
 - TxfLogCreateFileReadContext
---

# TxfLogCreateFileReadContext function


## -description

<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Creates a context to be used to read replication records.

## -parameters

### -param LogPath [in]

The path that identifies the Resource Manager's .blf file.

### -param BeginningLsn [in]

The first LSN in the range to be read.

### -param EndingLsn [in]

The last LSN in the range to be read.

### -param TxfFileId [in]

The TxF identifier to search for in the LSN range. For more information, see <a href="/windows/desktop/api/txfw32/ns-txfw32-txf_id">TXF_ID</a>.

### -param TxfLogContext [out]

A pointer to the context created.

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/txfw32/ns-txfw32-txf_id">TXF_ID</a>



<a href="/windows/desktop/api/txfw32/nf-txfw32-txflogdestroyreadcontext">TxfLogDestroyReadContext</a>