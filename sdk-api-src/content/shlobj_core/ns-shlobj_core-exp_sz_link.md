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

# EXP_SZ_LINK structure


## -description


Holds an extra data block used by <a href="https://msdn.microsoft.com/ac3279ad-1413-48bf-a830-4ec128352573">IShellLinkDataList</a>. It holds expandable environment strings for the icon or target.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the <b>EXP_SZ_LINK</b> structure.


### -field dwSignature

Type: <b>DWORD</b>

The structure's signature. It can have one of the following values.



#### EXP_SZ_LINK_SIG

Contains the link's target path.



#### EXP_SZ_ICON_SIG

Contains the links icon path.


### -field szTarget

Type: <b>__wchar_t[MAX_PATH]</b>

The null-terminated ANSI string with the path of the target or icon.


### -field swzTarget

Type: <b>WCHAR[MAX_PATH]</b>

The null-terminated Unicode string with the path of the target or icon.

