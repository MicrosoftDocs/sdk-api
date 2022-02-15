---
UID: NE:wbemcli.tag_WBEM_BACKUP_RESTORE_FLAGS
title: WBEM_BACKUP_RESTORE_FLAGS (wbemcli.h)
description: Contains flags used for the IWbemBackupRestore::Restore method and the IWbemBackupRestoreEx::Restore method.
helpviewer_keywords: ["WBEM_BACKUP_RESTORE_FLAGS","WBEM_BACKUP_RESTORE_FLAGS enumeration [Windows Management Instrumentation]","WBEM_FLAG_BACKUP_RESTORE_DEFAULT","WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN","wbemcli/WBEM_BACKUP_RESTORE_FLAGS","wbemcli/WBEM_FLAG_BACKUP_RESTORE_DEFAULT","wbemcli/WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN","wmi.wbem_backup_restore_flags"]
old-location: wmi\wbem_backup_restore_flags.htm
tech.root: wmi
ms.assetid: 00072B9F-B4AE-4308-9E8C-F61D982525B3
ms.date: 12/05/2018
ms.keywords: WBEM_BACKUP_RESTORE_FLAGS, WBEM_BACKUP_RESTORE_FLAGS enumeration [Windows Management Instrumentation], WBEM_FLAG_BACKUP_RESTORE_DEFAULT, WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, wbemcli/WBEM_BACKUP_RESTORE_FLAGS, wbemcli/WBEM_FLAG_BACKUP_RESTORE_DEFAULT, wbemcli/WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, wmi.wbem_backup_restore_flags
req.header: wbemcli.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: WBEM_BACKUP_RESTORE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tag_WBEM_BACKUP_RESTORE_FLAGS
 - wbemcli/tag_WBEM_BACKUP_RESTORE_FLAGS
 - WBEM_BACKUP_RESTORE_FLAGS
 - wbemcli/WBEM_BACKUP_RESTORE_FLAGS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_BACKUP_RESTORE_FLAGS
---

# WBEM_BACKUP_RESTORE_FLAGS enumeration


## -description

Contains flags used for the <a href="/windows/desktop/api/wbemcli/nf-wbemcli-iwbembackuprestore-restore">IWbemBackupRestore::Restore</a> method and the <a href="/previous-versions/windows/desktop/legacy/aa391421(v=vs.85)">IWbemBackupRestoreEx::Restore</a> method.

## -enum-fields

### -field WBEM_FLAG_BACKUP_RESTORE_DEFAULT:0

Does not shut down active clients; returns an error if there are any.

### -field WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN:1

Shuts down any active clients.
