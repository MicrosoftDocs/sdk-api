---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _FH_BACKUP_STATUS enumeration


## -description


Specifies whether File History backups are enabled.


## -enum-fields




### -field FH_STATUS_DISABLED

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

The <b>FH_STATUS_DISABLED_BY_GP</b> status can be queried by calling the <a href="https://msdn.microsoft.com/0AC8F205-B593-4117-9059-0DDA5BBE3124">IFhConfigMgr::GetBackupStatus</a> method, but it cannot be set by calling the <a href="https://msdn.microsoft.com/17FF01A1-028D-4A22-A64C-F24C98F86663">IFhConfigMgr::SetBackupStatus</a> method. This is because it can only be set by Group Policy.




## -see-also




<a href="https://msdn.microsoft.com/0AC8F205-B593-4117-9059-0DDA5BBE3124">IFhConfigMgr::GetBackupStatus</a>



<a href="https://msdn.microsoft.com/17FF01A1-028D-4A22-A64C-F24C98F86663">IFhConfigMgr::SetBackupStatus</a>
 

 

