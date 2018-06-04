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

# WindowInteractionState enumeration


## -description


Contains values that specify the current state of the window for purposes of user interaction.


## -enum-fields




### -field WindowInteractionState_Running

The window is running. This does not guarantee that the window is ready for user interaction or is responding. 


### -field WindowInteractionState_Closing

The window is closing.


### -field WindowInteractionState_ReadyForUserInteraction

The window is ready for user interaction.


### -field WindowInteractionState_BlockedByModalWindow

The window is blocked by a modal window.


### -field WindowInteractionState_NotResponding

The window is not responding.


## -see-also




<a href="https://msdn.microsoft.com/cf09ad4e-fd5b-4304-b5fb-165205bff1f3">IWindowProvider</a>
 

 

