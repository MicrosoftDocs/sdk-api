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

# tagWPC_ARGS_SETTINGSCHANGEEVENT enumeration


## -description


Indicates information about the changes to settings being made by a user.


## -enum-fields




### -field WPC_ARGS_SETTINGSCHANGEEVENT_CLASS

The class of change made to the setting.


### -field WPC_ARGS_SETTINGSCHANGEEVENT_SETTING

The setting that was changed.


### -field WPC_ARGS_SETTINGSCHANGEEVENT_OWNER

The user who made the change.


### -field WPC_ARGS_SETTINGSCHANGEEVENT_OLDVAL

The previous value of the setting that was changed.


### -field WPC_ARGS_SETTINGSCHANGEEVENT_NEWVAL

The new value of the setting that was changed.


### -field WPC_ARGS_SETTINGSCHANGEEVENT_REASON

The reason for the changed setting.


### -field WPC_ARGS_SETTINGSCHANGEEVENT_OPTIONAL

Optional information about the changed setting.


### -field WPC_ARGS_SETTINGSCHANGEEVENT_CARGS

The arguments of the changed setting.

