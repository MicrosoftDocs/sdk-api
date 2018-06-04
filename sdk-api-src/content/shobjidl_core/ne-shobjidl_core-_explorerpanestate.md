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

# _EXPLORERPANESTATE enumeration


## -description


Indicate flags used by <a href="https://msdn.microsoft.com/6c051cdc-b7f9-48dc-ba32-38f0f1ee5fda">IExplorerPaneVisibility::GetPaneState</a> to get the current state of the given Windows Explorer pane.


## -enum-fields




### -field EPS_DONTCARE

Do not make any modifications to the pane.


### -field EPS_DEFAULT_ON

Set the default state of the pane to "on", but respect any user-modified persisted state.


### -field EPS_DEFAULT_OFF

Set the default state of the pane to "off".


### -field EPS_STATEMASK

Unused.


### -field EPS_INITIALSTATE

Ignore any persisted state from the user, but the user can still modify the state.


### -field EPS_FORCE

Users cannot modify the state, that is, they do not have the ability to show or hide the given pane. This option implies EPS_INITIALSTATE.

