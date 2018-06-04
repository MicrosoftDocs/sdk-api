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



