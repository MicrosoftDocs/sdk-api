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

# _FH_RETENTION_TYPES enumeration


## -description


Specifies under what conditions previous versions of files and folders can be deleted from a backup target.


## -enum-fields




### -field FH_RETENTION_DISABLED

Previous versions are never deleted from the backup target.


### -field FH_RETENTION_UNLIMITED

The operating system can delete any previous version on an as-needed basis, unless it is the most recent version of a file that currently exists and is within the protection scope.


### -field FH_RETENTION_AGE_BASED

The operating system can delete any previous version older than the specified minimum age on as-needed basis, unless it is the most recent version of a file that  currently exists and is within the protection scope. The minimum age is specified by the <b>FH_RETENTION_AGE</b> local policy.


### -field MAX_RETENTION_TYPE

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.


## -remarks



The operating system deletes previous versions from a backup target only when the target is full or when the user has initiated data retention manually by using the File History item in Control Panel.

If <b>FH_RETENTION_AGE_BASED</b> is specified and the target is large enough, it is possible for the target to contain versions that are much older than the minimum age that is specified by the <b>FH_RETENTION_AGE</b> local policy.




## -see-also




<a href="https://msdn.microsoft.com/380B77C3-CA93-48D6-9915-FB788CF24C99">IFhConfigMgr::GetLocalPolicy</a>



<a href="https://msdn.microsoft.com/A1106349-6B14-4A44-B845-7853FA1919D6">IFhConfigMgr::SetLocalPolicy</a>
 

 

