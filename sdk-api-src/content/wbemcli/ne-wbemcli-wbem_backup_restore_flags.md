---
UID: NE:wbemcli.tag_WBEM_BACKUP_RESTORE_FLAGS
title: WBEM_BACKUP_RESTORE_FLAGS (wbemcli.h)
author: windows-sdk-content
description: Contains flags used for the IWbemBackupRestore::Restore method and the IWbemBackupRestoreEx::Restore method.
old-location: wmi\wbem_backup_restore_flags.htm
tech.root: WmiSdk
ms.assetid: 00072B9F-B4AE-4308-9E8C-F61D982525B3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WBEM_BACKUP_RESTORE_FLAGS, WBEM_BACKUP_RESTORE_FLAGS enumeration [Windows Management Instrumentation], WBEM_FLAG_BACKUP_RESTORE_DEFAULT, WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, wbemcli/WBEM_BACKUP_RESTORE_FLAGS, wbemcli/WBEM_FLAG_BACKUP_RESTORE_DEFAULT, wbemcli/WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, wmi.wbem_backup_restore_flags
ms.topic: enum
f1_keywords: 
 - "wbemcli/WBEM_BACKUP_RESTORE_FLAGS"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_BACKUP_RESTORE_FLAGS
targetos: Windows
req.typenames: WBEM_BACKUP_RESTORE_FLAGS
req.redist: 
ms.custom: 19H1
---

# WBEM_BACKUP_RESTORE_FLAGS enumeration


## -description


Contains flags used for the <a href="https://docs.microsoft.com/windows/desktop/api/wbemcli/nf-wbemcli-iwbembackuprestore-restore">IWbemBackupRestore::Restore</a> method and the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/aa391421(v=vs.85)">IWbemBackupRestoreEx::Restore</a> method.


## -enum-fields




### -field WBEM_FLAG_BACKUP_RESTORE_DEFAULT

Does not shut down active clients; returns an error if there are any.


### -field WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN

Shuts down any active clients.

