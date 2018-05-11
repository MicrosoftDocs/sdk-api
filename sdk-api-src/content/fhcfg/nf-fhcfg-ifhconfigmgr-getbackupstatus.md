---
UID: NF:fhcfg.IFhConfigMgr.GetBackupStatus
title: IFhConfigMgr::GetBackupStatus
author: windows-driver-content
description: Retrieves the backup status value for an FhConfigMgr object.
old-location: winprog\ifhconfigmgr_getbackupstatus.htm
old-project: DevNotes
ms.assetid: 0AC8F205-B593-4117-9059-0DDA5BBE3124
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: FhConfigMgr class [Windows API],GetBackupStatus method, GetBackupStatus, GetBackupStatus method [Windows API], GetBackupStatus method [Windows API],FhConfigMgr class, GetBackupStatus method [Windows API],IFhConfigMgr interface, IFhConfigMgr interface [Windows API],GetBackupStatus method, IFhConfigMgr.GetBackupStatus, IFhConfigMgr::GetBackupStatus, fhcfg/IFhConfigMgr::GetBackupStatus, winprog.ifhconfigmgr_getbackupstatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FH_TARGET_PROPERTY_TYPE, *PFH_TARGET_PROPERTY_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Fhcfg.h
api_name:
-	IFhConfigMgr.GetBackupStatus
-	FhConfigMgr.GetBackupStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 5
---

# IFhConfigMgr::GetBackupStatus


## -description


Retrieves the backup status value for an <a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a> object.


## -parameters




### -param BackupStatus [out]

Receives the backup status value. See the <a href="https://msdn.microsoft.com/7F988CA1-8295-4758-B66B-9B707B2CA126">FH_BACKUP_STATUS</a> enumeration for the list of possible backup status values.


## -returns



<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.




## -see-also




<a href="https://msdn.microsoft.com/7F988CA1-8295-4758-B66B-9B707B2CA126">FH_BACKUP_STATUS</a>



<a href="https://msdn.microsoft.com/CC97FC0F-3AA4-4D8A-81B3-14F68FDF5788">FhConfigMgr</a>



<a href="https://msdn.microsoft.com/CDE8A011-6E78-49DF-A5E1-8E968355BA11">IFhConfigMgr</a>



<a href="https://msdn.microsoft.com/17FF01A1-028D-4A22-A64C-F24C98F86663">IFhConfigMgr::SetBackupStatus</a>
 

 

