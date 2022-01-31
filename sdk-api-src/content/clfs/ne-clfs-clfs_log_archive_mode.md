---
UID: NE:clfs._CLFS_LOG_ARCHIVE_MODE
title: CLFS_LOG_ARCHIVE_MODE (clfs.h)
description: Specifies whether a log is ephemeral.
helpviewer_keywords: ["*PCLFS_LOG_ARCHIVE_MODE","CLFS_LOG_ARCHIVE_MODE","CLFS_LOG_ARCHIVE_MODE enumeration [Files]","ClfsLogArchiveDisabled","ClfsLogArchiveEnabled","PCLFS_LOG_ARCHIVE_MODE","PCLFS_LOG_ARCHIVE_MODE enumeration pointer [Files]","clfs/CLFS_LOG_ARCHIVE_MODE","clfs/ClfsLogArchiveDisabled","clfs/ClfsLogArchiveEnabled","clfs/PCLFS_LOG_ARCHIVE_MODE","fs.clfs_log_archive_mode"]
old-location: fs\clfs_log_archive_mode.htm
tech.root: fs
ms.assetid: 448d79cd-d959-4585-877e-0f70b44f3172
ms.date: 12/05/2018
ms.keywords: '*PCLFS_LOG_ARCHIVE_MODE, CLFS_LOG_ARCHIVE_MODE, CLFS_LOG_ARCHIVE_MODE enumeration [Files], ClfsLogArchiveDisabled, ClfsLogArchiveEnabled, PCLFS_LOG_ARCHIVE_MODE, PCLFS_LOG_ARCHIVE_MODE enumeration pointer [Files], clfs/CLFS_LOG_ARCHIVE_MODE, clfs/ClfsLogArchiveDisabled, clfs/ClfsLogArchiveEnabled, clfs/PCLFS_LOG_ARCHIVE_MODE, fs.clfs_log_archive_mode'
req.header: clfs.h
req.include-header: 
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
req.typenames: CLFS_LOG_ARCHIVE_MODE, *PCLFS_LOG_ARCHIVE_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CLFS_LOG_ARCHIVE_MODE
 - clfs/_CLFS_LOG_ARCHIVE_MODE
 - PCLFS_LOG_ARCHIVE_MODE
 - clfs/PCLFS_LOG_ARCHIVE_MODE
 - CLFS_LOG_ARCHIVE_MODE
 - clfs/CLFS_LOG_ARCHIVE_MODE
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
 - CLFS_LOG_ARCHIVE_MODE
---

# CLFS_LOG_ARCHIVE_MODE enumeration


## -description

Specifies whether a log is ephemeral.

## -enum-fields

### -field ClfsLogArchiveEnabled:0x01

Enables log archive (ephemeral logs) support.

### -field ClfsLogArchiveDisabled:0x02

Disables ephemeral logs.

## -see-also

<a href="/windows/desktop/api/clfsw32/nf-clfsw32-setlogarchivemode">SetLogArchiveMode</a>
