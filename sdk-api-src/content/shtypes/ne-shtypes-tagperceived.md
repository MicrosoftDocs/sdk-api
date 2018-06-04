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

# tagPERCEIVED enumeration


## -description


Specifies a file's perceived type. This set of constants is used in the <a href="https://msdn.microsoft.com/d37f1574-b261-43bf-9712-05a569ab4246">AssocGetPerceivedType</a> function.


## -enum-fields




### -field PERCEIVED_TYPE_FIRST


### -field PERCEIVED_TYPE_CUSTOM

The file's perceived type as defined in the registry is not a known type.


### -field PERCEIVED_TYPE_UNSPECIFIED

The file does not have a perceived type.


### -field PERCEIVED_TYPE_FOLDER

Not used.


### -field PERCEIVED_TYPE_UNKNOWN

The file's perceived type hasn't yet been requested. This is the cached type of the object when it is created. This value is never returned by <a href="https://msdn.microsoft.com/d37f1574-b261-43bf-9712-05a569ab4246">AssocGetPerceivedType</a>.


### -field PERCEIVED_TYPE_TEXT

The file's perceived type is "text".


### -field PERCEIVED_TYPE_IMAGE

The file's perceived type is "image".


### -field PERCEIVED_TYPE_AUDIO

The file's perceived type is "audio".


### -field PERCEIVED_TYPE_VIDEO

The file's perceived type is "video".


### -field PERCEIVED_TYPE_COMPRESSED

The file's perceived type is "compressed".


### -field PERCEIVED_TYPE_DOCUMENT

The file's perceived type is "document".


### -field PERCEIVED_TYPE_SYSTEM

The file's perceived type is "system".


### -field PERCEIVED_TYPE_APPLICATION

The file's perceived type is "application".


### -field PERCEIVED_TYPE_GAMEMEDIA

<b>Windows Vista and later</b>. The file's perceived type is "gamemedia".


### -field PERCEIVED_TYPE_CONTACTS

<b>Windows Vista and later</b>.The file's perceived type is "contacts"


### -field PERCEIVED_TYPE_LAST




## -remarks



Prior to Windows Vista, this enumeration was declared in Shlwapi.h.



