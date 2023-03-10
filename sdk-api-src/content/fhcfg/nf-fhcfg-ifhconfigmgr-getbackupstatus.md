---
UID: NF:fhcfg.IFhConfigMgr.GetBackupStatus
title: IFhConfigMgr::GetBackupStatus (fhcfg.h)
description: Retrieves the backup status value for an FhConfigMgr object.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","GetBackupStatus method","GetBackupStatus","GetBackupStatus method [Windows API]","GetBackupStatus method [Windows API]","FhConfigMgr class","GetBackupStatus method [Windows API]","IFhConfigMgr interface","IFhConfigMgr interface [Windows API]","GetBackupStatus method","IFhConfigMgr.GetBackupStatus","IFhConfigMgr::GetBackupStatus","fhcfg/IFhConfigMgr::GetBackupStatus","winprog.ifhconfigmgr_getbackupstatus"]
old-location: winprog\ifhconfigmgr_getbackupstatus.htm
tech.root: winprog
ms.assetid: 0AC8F205-B593-4117-9059-0DDA5BBE3124
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],GetBackupStatus method, GetBackupStatus, GetBackupStatus method [Windows API], GetBackupStatus method [Windows API],FhConfigMgr class, GetBackupStatus method [Windows API],IFhConfigMgr interface, IFhConfigMgr interface [Windows API],GetBackupStatus method, IFhConfigMgr.GetBackupStatus, IFhConfigMgr::GetBackupStatus, fhcfg/IFhConfigMgr::GetBackupStatus, winprog.ifhconfigmgr_getbackupstatus
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFhConfigMgr::GetBackupStatus
 - fhcfg/IFhConfigMgr::GetBackupStatus
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.GetBackupStatus
 - FhConfigMgr.GetBackupStatus
---

# IFhConfigMgr::GetBackupStatus


## -description

Retrieves the backup status value for an <a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param BackupStatus [out]

Receives the backup status value. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_backup_status">FH_BACKUP_STATUS</a> enumeration for the list of possible backup status values.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_backup_status">FH_BACKUP_STATUS</a>



<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setbackupstatus">IFhConfigMgr::SetBackupStatus</a>