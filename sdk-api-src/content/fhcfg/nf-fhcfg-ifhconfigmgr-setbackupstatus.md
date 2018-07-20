---
UID: NF:fhcfg.IFhConfigMgr.SetBackupStatus
title: IFhConfigMgr::SetBackupStatus
author: windows-sdk-content
description: Changes the backup status value for an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_setbackupstatus.htm
old-project: devnotes
ms.assetid: 17FF01A1-028D-4A22-A64C-F24C98F86663
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: FhConfigMgr class [Windows API],SetBackupStatus method, IFhConfigMgr interface [Windows API],SetBackupStatus method, IFhConfigMgr.SetBackupStatus, IFhConfigMgr::SetBackupStatus, SetBackupStatus, SetBackupStatus method [Windows API], SetBackupStatus method [Windows API],FhConfigMgr class, SetBackupStatus method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::SetBackupStatus, winprog.ifhconfigmgr_setbackupstatus
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
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
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhConfigMgr::SetBackupStatus


## -description


Changes the backup status value for an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.


## -parameters




### -param BackupStatus [in]

The backup status value. See the <a href="https://msdn.microsoft.com/7F988CA1-8295-4758-B66B-9B707B2CA126">FH_BACKUP_STATUS</a> enumeration for a list of possible backup status values.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -remarks



<b>FH_STATUS_DISABLED_BY_GP</b> is not a valid value for the <i>BackupStatus</i> parameter.




## -see-also




<a href="https://msdn.microsoft.com/7F988CA1-8295-4758-B66B-9B707B2CA126">FH_BACKUP_STATUS</a>



<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/0AC8F205-B593-4117-9059-0DDA5BBE3124">IFhConfigMgr::GetBackupStatus</a>
 

 

