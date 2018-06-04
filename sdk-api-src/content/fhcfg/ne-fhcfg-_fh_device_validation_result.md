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

# _FH_DEVICE_VALIDATION_RESULT enumeration


## -description


Indicates whether the  storage device or network share can be used as a File History backup target.


## -enum-fields




### -field FH_ACCESS_DENIED

The storage device or network share cannot be used as a backup target, because it is not accessible.


### -field FH_INVALID_DRIVE_TYPE

The storage device or network share cannot be used as a backup target, because the drive type is not supported.  For example, a CD or DVD cannot be used as a  File History backup target.


### -field FH_READ_ONLY_PERMISSION

The storage device or network share cannot be used as a backup target, because it is read-only.


### -field FH_CURRENT_DEFAULT

The storage device or network share is already being used as a backup target.


### -field FH_NAMESPACE_EXISTS

The storage device or network share was previously used to back up files from a computer or user that has the same name as the current computer or user. It can be used as a backup target, but if it is used, the operating system will delete the previous backup.


### -field FH_TARGET_PART_OF_LIBRARY

The storage device or network share cannot be used as a backup target, because it is in the File History protection scope.


### -field FH_VALID_TARGET

The storage device or network share can be used as a backup target.


### -field MAX_VALIDATION_RESULT

The maximum enumeration value for this enumeration. This value and all values greater than it are reserved for system use.


## -see-also




<a href="https://msdn.microsoft.com/EC41C4EE-A909-4DD4-AA32-5054BBEAF421">IFhConfigMgr::ValidateTarget</a>
 

 

