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

# SHARE_ROLE enumeration


## -description


Specifies the access permissions assigned to the <b>Users</b> or <b>Public</b> folder. Used in <a href="https://msdn.microsoft.com/81bcd470-3fb8-4c6d-af4f-6f11206fa40a">CreateShare</a> and <a href="https://msdn.microsoft.com/d9ca5acf-2dd1-4fbe-a67f-91578d68b955">GetSharePermissions</a>.


## -enum-fields




### -field SHARE_ROLE_INVALID

The folder is not shared.


### -field SHARE_ROLE_READER

The contents of the folder can be read, but not altered or added to.


### -field SHARE_ROLE_CONTRIBUTOR

The contents of the folder can be read and altered. New items can be added, however items can be deleted only by the user that contributed them.


### -field SHARE_ROLE_CO_OWNER

The contents of the folder can be read, changed, or added to.


### -field SHARE_ROLE_OWNER

Not normally used in the context of this interface.


### -field SHARE_ROLE_CUSTOM

The folder is shared, but the share role is neither SHARE_ROLE_READER, SHARE_ROLE_CONTRIBUTOR, or SHARE_ROLE_CO_OWNER.


### -field SHARE_ROLE_MIXED

Not used in the context of this interface.


## -remarks




<a href="https://msdn.microsoft.com/81bcd470-3fb8-4c6d-af4f-6f11206fa40a">ISharingConfigurationManager::CreateShare</a> accepts only <b>SHARE_ROLE_READER</b> and <b>SHARE_ROLE_CO_OWNER</b>. All other values are seen only in the results of <a href="https://msdn.microsoft.com/d9ca5acf-2dd1-4fbe-a67f-91578d68b955">ISharingConfigurationManager::GetSharePermissions</a>.



