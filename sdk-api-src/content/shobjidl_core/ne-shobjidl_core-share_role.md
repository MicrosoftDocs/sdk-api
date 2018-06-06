---
UID: NE:shobjidl_core.SHARE_ROLE
title: SHARE_ROLE
author: windows-sdk-content
description: Specifies the access permissions assigned to the Users or Public folder. Used in CreateShare and GetSharePermissions.
old-location: shell\SHARE_ROLE.htm
old-project: shell
ms.assetid: d1c8764d-002e-4fbd-a0a6-1f469f8b1fbb
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: SHARE_ROLE, SHARE_ROLE enumeration [Windows Shell], SHARE_ROLE_CONTRIBUTOR, SHARE_ROLE_CO_OWNER, SHARE_ROLE_CUSTOM, SHARE_ROLE_INVALID, SHARE_ROLE_MIXED, SHARE_ROLE_OWNER, SHARE_ROLE_READER, _shell_SHARE_ROLE, shell.SHARE_ROLE, shobjidl_core/SHARE_ROLE, shobjidl_core/SHARE_ROLE_CONTRIBUTOR, shobjidl_core/SHARE_ROLE_CO_OWNER, shobjidl_core/SHARE_ROLE_CUSTOM, shobjidl_core/SHARE_ROLE_INVALID, shobjidl_core/SHARE_ROLE_MIXED, shobjidl_core/SHARE_ROLE_OWNER, shobjidl_core/SHARE_ROLE_READER
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: SHARE_ROLE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - SHARE_ROLE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Internet Explorer 6.01
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



