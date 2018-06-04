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

# INTERACTION_STATE enumeration


## -description


Specifies the state of the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -enum-fields




### -field INTERACTION_STATE_IDLE

There are no ongoing interactions and all transitional states (inertia, double tap) are complete. It is safe to reuse the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


### -field INTERACTION_STATE_IN_INTERACTION

There is an ongoing interaction. One or more contacts are detected, or inertia is in progress.


### -field INTERACTION_STATE_POSSIBLE_DOUBLE_TAP

All contacts are lifted, but the time threshold for double tap has not been crossed.


### -field INTERACTION_STATE_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://msdn.microsoft.com/35d581a9-b1be-4f9b-8783-ccea3469921a">GetStateInteractionContext</a>



<a href="https://msdn.microsoft.com/0B8D9A5F-F7CF-42B0-A320-77D44445CC24">Interaction Context Enumerations</a>
 

 

