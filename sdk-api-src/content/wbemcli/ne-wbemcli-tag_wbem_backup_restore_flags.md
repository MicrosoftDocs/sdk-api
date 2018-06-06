---
UID: NE:wbemcli.tag_WBEM_BACKUP_RESTORE_FLAGS
title: tag_WBEM_BACKUP_RESTORE_FLAGS
author: windows-sdk-content
description: Contains flags used for the IWbemBackupRestore::Restore method and the IWbemBackupRestoreEx::Restore method.
old-location: wmi\wbem_backup_restore_flags.htm
old-project: WmiSdk
ms.assetid: 00072B9F-B4AE-4308-9E8C-F61D982525B3
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: WBEM_BACKUP_RESTORE_FLAGS, WBEM_BACKUP_RESTORE_FLAGS enumeration [Windows Management Instrumentation], WBEM_FLAG_BACKUP_RESTORE_DEFAULT, WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, tag_WBEM_BACKUP_RESTORE_FLAGS, wbemcli/WBEM_BACKUP_RESTORE_FLAGS, wbemcli/WBEM_FLAG_BACKUP_RESTORE_DEFAULT, wbemcli/WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN, wmi.wbem_backup_restore_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: WBEM_BACKUP_RESTORE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wbemcli.h
api_name:
 - WBEM_BACKUP_RESTORE_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tag_WBEM_BACKUP_RESTORE_FLAGS enumeration


## -description


Contains flags used for the <a href="https://msdn.microsoft.com/73a61c69-0a78-4c38-aaec-a72b644f19b4">IWbemBackupRestore::Restore</a> method and the <a href="https://msdn.microsoft.com/9cc85100-5964-4c76-a0e5-305ee7b1638d">IWbemBackupRestoreEx::Restore</a> method.


## -enum-fields




### -field WBEM_FLAG_BACKUP_RESTORE_DEFAULT

Does not shut down active clients; returns an error if there are any.


### -field WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN

Shuts down any active clients.

