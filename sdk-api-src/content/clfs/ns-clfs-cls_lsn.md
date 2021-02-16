---
UID: NS:clfs._CLS_LSN
title: CLS_LSN (clfs.h)
description: Represents a valid log address.
helpviewer_keywords: ["*PCLFS_LSN","*PCLS_LSN","CLFS_LSN","CLFS_LSN structure [Files]","CLS_LSN","PCLFS_LSN","PCLFS_LSN structure pointer [Files]","PPCLS_LSN","clfs/CLFS_LSN","clfs/PCLFS_LSN","fs.clfs_lsn"]
old-location: fs\clfs_lsn.htm
tech.root: fs
ms.assetid: f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a
ms.date: 12/05/2018
ms.keywords: '*PCLFS_LSN, *PCLS_LSN, CLFS_LSN, CLFS_LSN structure [Files], CLS_LSN, PCLFS_LSN, PCLFS_LSN structure pointer [Files], PPCLS_LSN, clfs/CLFS_LSN, clfs/PCLFS_LSN, fs.clfs_lsn'
req.header: clfs.h
req.include-header: Clfsw32.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
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
req.typenames: CLS_LSN, *PCLS_LSN, PPCLS_LSN
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLS_LSN
 - clfs/_CLS_LSN
 - PCLS_LSN
 - clfs/PCLS_LSN
 - CLS_LSN
 - clfs/CLS_LSN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Clfs.h
api_name:
 - CLFS_LSN
---

# CLS_LSN structure


## -description

Represents a valid log address.

## -struct-fields

### -field Internal

The log sequence number (LSN).

## -remarks

The LSN is the valid address that is  unique to a client, and returned after the client appends a record to the log.  The address remains valid if the system does not fail, or its marshaled log buffer is  flushed successfully to disk.

In log streams, LSNs increase  monotonically. You cannot compare  LSNs between  log streams.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-lsncreate">LsnCreate</a>