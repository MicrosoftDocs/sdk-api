---
UID: NE:shobjidl_core.DEF_SHARE_ID
title: DEF_SHARE_ID
author: windows-sdk-content
description: Values that specify the folder being acted on by methods of the ISharingConfigurationManager interface.
old-location: shell\DEF_SHARE_ID.htm
tech.root: shell
ms.assetid: 02d3b664-eeef-4214-99e8-246241103c4e
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: DEFSHAREID_PUBLIC, DEFSHAREID_USERS, DEF_SHARE_ID, DEF_SHARE_ID enumeration [Windows Shell], _shell_DEF_SHARE_ID, shell.DEF_SHARE_ID, shobjidl_core/DEFSHAREID_PUBLIC, shobjidl_core/DEFSHAREID_USERS, shobjidl_core/DEF_SHARE_ID
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - shobjidl_core.h
api_name:
 - DEF_SHARE_ID
product: Windows
targetos: Windows
req.typenames: DEF_SHARE_ID
req.redist: 
---

# DEF_SHARE_ID enumeration


## -description


Values that specify the folder being acted on by methods of the <a href="https://msdn.microsoft.com/64bf628d-4e9b-42a8-a9cf-04d321645d9a">ISharingConfigurationManager</a> interface.


## -enum-fields




### -field DEFSHAREID_USERS

The <b>Users</b> folder (<a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">FOLDERID_UserProfiles</a>). This folder is usually found at C:\Users.


### -field DEFSHAREID_PUBLIC

The <b>Public</b> folder (<a href="https://msdn.microsoft.com/f2c08ade-3083-44e4-82b0-dde45f0e3094">FOLDERID_Public</a>). This folder is usually found at C:\Users\Public.


## -remarks



In Windows Vista, an Server Message Block (SMB) share is created for both the <b>Users</b> and <b>Public</b> folders. As of Windows 7, the Public share is accessed through the Users share, so only <b>Users</b> is given an SMB share.

When methods are called with the <b>DEFSHAREID_PUBLIC</b> value, the restrictions specified by the <a href="https://msdn.microsoft.com/d1c8764d-002e-4fbd-a0a6-1f469f8b1fbb">SHARE_ROLE</a> value in that call apply to the <i>Everyone</i> access control entry (ACE).

When methods are called with the <b>DEFSHAREID_USERS</b> value, the restrictions specified by the <a href="https://msdn.microsoft.com/d1c8764d-002e-4fbd-a0a6-1f469f8b1fbb">SHARE_ROLE</a> value in that call apply to the <i>Authenticated Users</i> ACE.



