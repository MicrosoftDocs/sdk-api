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

# PLACEHOLDER_STATES enumeration


## -description


Specifies the states that a placeholder file can have. Retrieve this value through the System.FilePlaceholderStatus (PKEY_FilePlaceholderStatus) property.


## -enum-fields




### -field PS_NONE

None of the other states apply at this time.


### -field PS_MARKED_FOR_OFFLINE_AVAILABILITY

May already be or eventually will be available offline.


### -field PS_FULL_PRIMARY_STREAM_AVAILABLE

The primary stream has been made fully available.


### -field PS_CREATE_FILE_ACCESSIBLE

The file is accessible through a call to the <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, without requesting the opening of reparse points.


### -field PS_CLOUDFILE_PLACEHOLDER


### -field PS_DEFAULT


### -field PS_ALL

A bitmask value for all valid PLACEHOLDER_STATES flags.

