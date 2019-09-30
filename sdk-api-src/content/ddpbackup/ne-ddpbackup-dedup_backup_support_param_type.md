---
UID: NE:ddpbackup._DEDUP_BACKUP_SUPPORT_PARAM_TYPE
title: DEDUP_BACKUP_SUPPORT_PARAM_TYPE (ddpbackup.h)
author: windows-sdk-content
description: Indicates whether Data Deduplication should perform an unoptimized or optimized restore.
old-location: dedup\dedup_backup_support_param_type.htm
tech.root: dedup
ms.assetid: 654663C4-1E28-435A-9D81-1E390BC66B62
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DEDUP_BACKUP_SUPPORT_PARAM_TYPE, DEDUP_BACKUP_SUPPORT_PARAM_TYPE enumeration [Data Deduplication API], DEDUP_RECONSTRUCT_OPTIMIZED, DEDUP_RECONSTRUCT_UNOPTIMIZED, ddpbackup/DEDUP_BACKUP_SUPPORT_PARAM_TYPE, ddpbackup/DEDUP_RECONSTRUCT_OPTIMIZED, ddpbackup/DEDUP_RECONSTRUCT_UNOPTIMIZED, dedup.dedup_backup_support_param_type
ms.topic: enum
f1_keywords: 
 - "ddpbackup/DEDUP_BACKUP_SUPPORT_PARAM_TYPE"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - DdpBackup.h
api_name:
 - DEDUP_BACKUP_SUPPORT_PARAM_TYPE
targetos: Windows
req.typenames: DEDUP_BACKUP_SUPPORT_PARAM_TYPE
req.redist: 
ms.custom: 19H1
---

# DEDUP_BACKUP_SUPPORT_PARAM_TYPE enumeration


## -description


Indicates whether Data Deduplication should perform an unoptimized or optimized restore.


## -enum-fields




### -field DEDUP_RECONSTRUCT_UNOPTIMIZED

Perform an unoptimized restore.


### -field DEDUP_RECONSTRUCT_OPTIMIZED

Reserved for future use. Do not use.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ddpbackup/nf-ddpbackup-idedupbackupsupport-restorefiles">IDedupBackupSupport::RestoreFiles</a>
 

 

