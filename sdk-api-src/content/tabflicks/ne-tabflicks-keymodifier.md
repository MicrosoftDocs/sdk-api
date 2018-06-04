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

# KEYMODIFIER enumeration


## -description



Determines which, if any, modifier keys were pressed when the flick gesture occurred.




## -enum-fields




### -field KEYMODIFIER_CONTROL

The Control key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_MENU

The Menu key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_SHIFT

The Shift key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_WIN

The Windows key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_ALTGR

The Alt key was pressed when the Flicks gesture occurred.


### -field KEYMODIFIER_EXT

The pressed key's scan code was preceded by a prefix byte that has the value 0xE0 (224).


