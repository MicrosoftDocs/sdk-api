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

# tag_WBEM_BACKUP_RESTORE_FLAGS enumeration


## -description


Contains flags used for the <a href="https://msdn.microsoft.com/73a61c69-0a78-4c38-aaec-a72b644f19b4">IWbemBackupRestore::Restore</a> method and the <a href="https://msdn.microsoft.com/9cc85100-5964-4c76-a0e5-305ee7b1638d">IWbemBackupRestoreEx::Restore</a> method.


## -enum-fields




### -field WBEM_FLAG_BACKUP_RESTORE_DEFAULT

Does not shut down active clients; returns an error if there are any.


### -field WBEM_FLAG_BACKUP_RESTORE_FORCE_SHUTDOWN

Shuts down any active clients.

