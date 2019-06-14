---
UID: NF:fhcfg.IFhConfigMgr.SetBackupStatus
title: IFhConfigMgr::SetBackupStatus (fhcfg.h)
author: windows-sdk-content
description: Changes the backup status value for an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_setbackupstatus.htm
tech.root: DevNotes
ms.assetid: 17FF01A1-028D-4A22-A64C-F24C98F86663
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],SetBackupStatus method, IFhConfigMgr interface [Windows API],SetBackupStatus method, IFhConfigMgr.SetBackupStatus, IFhConfigMgr::SetBackupStatus, SetBackupStatus, SetBackupStatus method [Windows API], SetBackupStatus method [Windows API],FhConfigMgr class, SetBackupStatus method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::SetBackupStatus, winprog.ifhconfigmgr_setbackupstatus
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.SetBackupStatus
 - FhConfigMgr.SetBackupStatus
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFhConfigMgr::SetBackupStatus


## -description


Changes the backup status value for an <a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.


## -parameters




### -param BackupStatus [in]

The backup status value. See the <a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/ne-fhcfg-_fh_backup_status">FH_BACKUP_STATUS</a> enumeration for a list of possible backup status values.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



<b>FH_STATUS_DISABLED_BY_GP</b> is not a valid value for the <i>BackupStatus</i> parameter.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/ne-fhcfg-_fh_backup_status">FH_BACKUP_STATUS</a>



<a href="https://docs.microsoft.com/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="https://docs.microsoft.com/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getbackupstatus">IFhConfigMgr::GetBackupStatus</a>
 

 

