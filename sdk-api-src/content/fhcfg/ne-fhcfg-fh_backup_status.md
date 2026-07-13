---
UID: NE:fhcfg._FH_BACKUP_STATUS
title: FH_BACKUP_STATUS (fhcfg.h)
description: Specifies whether File History backups are enabled.
helpviewer_keywords: ["FH_BACKUP_STATUS","FH_BACKUP_STATUS enumeration [Windows API]","FH_STATUS_DISABLED","FH_STATUS_DISABLED_BY_GP","FH_STATUS_ENABLED","MAX_BACKUP_STATUS","fhcfg/FH_BACKUP_STATUS","fhcfg/FH_STATUS_DISABLED","fhcfg/FH_STATUS_DISABLED_BY_GP","fhcfg/FH_STATUS_ENABLED","fhcfg/MAX_BACKUP_STATUS","winprog.fh_backup_status"]
old-location: winprog\fh_backup_status.htm
tech.root: winprog
ms.assetid: 7F988CA1-8295-4758-B66B-9B707B2CA126
ms.date: 12/05/2018
ms.keywords: FH_BACKUP_STATUS, FH_BACKUP_STATUS enumeration [Windows API], FH_STATUS_DISABLED, FH_STATUS_DISABLED_BY_GP, FH_STATUS_ENABLED, MAX_BACKUP_STATUS, fhcfg/FH_BACKUP_STATUS, fhcfg/FH_STATUS_DISABLED, fhcfg/FH_STATUS_DISABLED_BY_GP, fhcfg/FH_STATUS_ENABLED, fhcfg/MAX_BACKUP_STATUS, winprog.fh_backup_status
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FH_BACKUP_STATUS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FH_BACKUP_STATUS
 - fhcfg/_FH_BACKUP_STATUS
 - FH_BACKUP_STATUS
 - fhcfg/FH_BACKUP_STATUS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Fhcfg.h
api_name:
 - FH_BACKUP_STATUS
---

# FH_BACKUP_STATUS enumeration


## -description

Specifies whether File History backups are enabled.

## -enum-fields

### -field FH_STATUS_DISABLED:0

File History backups are not enabled by the user.

### -field FH_STATUS_DISABLED_BY_GP

File History backups are disabled by Group Policy.

### -field FH_STATUS_ENABLED

File History backups are enabled.

### -field FH_STATUS_REHYDRATING

### -field MAX_BACKUP_STATUS

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.

## -remarks

The protection scope is the set of files and folders that  are backed up by the File History feature. The default protection scope includes all folders from all user libraries and the  Contacts, Desktop, and Favorites folders.

The <b>FH_STATUS_DISABLED_BY_GP</b> status can be queried by calling the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getbackupstatus">IFhConfigMgr::GetBackupStatus</a> method, but it cannot be set by calling the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setbackupstatus">IFhConfigMgr::SetBackupStatus</a> method. This is because it can only be set by Group Policy.

## -see-also

<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getbackupstatus">IFhConfigMgr::GetBackupStatus</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setbackupstatus">IFhConfigMgr::SetBackupStatus</a>
