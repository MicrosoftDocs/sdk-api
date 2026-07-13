---
UID: NE:ddpbackup._DEDUP_BACKUP_SUPPORT_PARAM_TYPE
title: DEDUP_BACKUP_SUPPORT_PARAM_TYPE (ddpbackup.h)
description: Indicates whether Data Deduplication should perform an unoptimized or optimized restore.
helpviewer_keywords: ["DEDUP_BACKUP_SUPPORT_PARAM_TYPE","DEDUP_BACKUP_SUPPORT_PARAM_TYPE enumeration [Data Deduplication API]","DEDUP_RECONSTRUCT_OPTIMIZED","DEDUP_RECONSTRUCT_UNOPTIMIZED","ddpbackup/DEDUP_BACKUP_SUPPORT_PARAM_TYPE","ddpbackup/DEDUP_RECONSTRUCT_OPTIMIZED","ddpbackup/DEDUP_RECONSTRUCT_UNOPTIMIZED","dedup.dedup_backup_support_param_type"]
old-location: dedup\dedup_backup_support_param_type.htm
tech.root: dedup
ms.assetid: 654663C4-1E28-435A-9D81-1E390BC66B62
ms.date: 12/05/2018
ms.keywords: DEDUP_BACKUP_SUPPORT_PARAM_TYPE, DEDUP_BACKUP_SUPPORT_PARAM_TYPE enumeration [Data Deduplication API], DEDUP_RECONSTRUCT_OPTIMIZED, DEDUP_RECONSTRUCT_UNOPTIMIZED, ddpbackup/DEDUP_BACKUP_SUPPORT_PARAM_TYPE, ddpbackup/DEDUP_RECONSTRUCT_OPTIMIZED, ddpbackup/DEDUP_RECONSTRUCT_UNOPTIMIZED, dedup.dedup_backup_support_param_type
req.header: ddpbackup.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DdpBackup.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: DEDUP_BACKUP_SUPPORT_PARAM_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DEDUP_BACKUP_SUPPORT_PARAM_TYPE
 - ddpbackup/_DEDUP_BACKUP_SUPPORT_PARAM_TYPE
 - DEDUP_BACKUP_SUPPORT_PARAM_TYPE
 - ddpbackup/DEDUP_BACKUP_SUPPORT_PARAM_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DdpBackup.h
api_name:
 - DEDUP_BACKUP_SUPPORT_PARAM_TYPE
---

# DEDUP_BACKUP_SUPPORT_PARAM_TYPE enumeration


## -description

Indicates whether Data Deduplication should perform an unoptimized or optimized restore.

## -enum-fields

### -field DEDUP_RECONSTRUCT_UNOPTIMIZED:1

Perform an unoptimized restore.

### -field DEDUP_RECONSTRUCT_OPTIMIZED:2

Reserved for future use. Do not use.

## -see-also

<a href="/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">IDedupBackupSupport::RestoreFiles</a>
