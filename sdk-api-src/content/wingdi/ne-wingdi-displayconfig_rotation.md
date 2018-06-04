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

# DISPLAYCONFIG_ROTATION enumeration


## -description


The DISPLAYCONFIG_ROTATION enumeration specifies the clockwise rotation of the display.


## -enum-fields




### -field DISPLAYCONFIG_ROTATION_IDENTITY

Indicates that rotation is 0 degrees—landscape mode.


### -field DISPLAYCONFIG_ROTATION_ROTATE90

Indicates that rotation is 90 degrees clockwise—portrait mode.


### -field DISPLAYCONFIG_ROTATION_ROTATE180

Indicates that rotation is 180 degrees clockwise—inverted landscape mode.


### -field DISPLAYCONFIG_ROTATION_ROTATE270

Indicates that rotation is 270 degrees clockwise—inverted portrait mode.


### -field DISPLAYCONFIG_ROTATION_FORCE_UINT32

Forces this enumeration to compile to 32 bits in size. Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits. You should not use this value.

