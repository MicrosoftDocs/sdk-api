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

# INERTIA_PARAMETER enumeration


## -description


Specifies the inertia values for a manipulation (translation, rotation, scaling).


## -enum-fields




### -field INERTIA_PARAMETER_TRANSLATION_DECELERATION

The rate of deceleration, in degrees/ms².


### -field INERTIA_PARAMETER_TRANSLATION_DISPLACEMENT

The relative change in screen location, in DIPs.


### -field INERTIA_PARAMETER_ROTATION_DECELERATION

The rate of deceleration, in degrees/ms².


### -field INERTIA_PARAMETER_ROTATION_ANGLE

The relative change in angle of rotation, in radians.


### -field INERTIA_PARAMETER_EXPANSION_DECELERATION

The rate of deceleration, in degrees/ms².


### -field INERTIA_PARAMETER_EXPANSION_EXPANSION

The relative change in size, in pixels.


### -field INERTIA_PARAMETER_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://msdn.microsoft.com/0B8D9A5F-F7CF-42B0-A320-77D44445CC24">Interaction Context Enumerations</a>



<a href="https://msdn.microsoft.com/5b228339-3830-407f-a8ea-55f40156cc32">SetInertiaParameterInteractionContext</a>
 

 

