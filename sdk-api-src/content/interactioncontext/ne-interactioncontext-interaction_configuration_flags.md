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

# INTERACTION_CONFIGURATION_FLAGS enumeration


## -description


Specifies the interactions to enable when configuring an <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -enum-fields




### -field INTERACTION_CONFIGURATION_FLAG_NONE

No interactions enabled.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION

All manipulations enabled (move, rotate, and scale).


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_TRANSLATION_X

Translate (move) along the x-axis.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_TRANSLATION_Y

Translate (move) along the y-axis.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_ROTATION

Rotation.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_SCALING

Scaling.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_TRANSLATION_INERTIA

Translation inertia (in direction of move) after contact lifted.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_ROTATION_INERTIA

Rotation inertia after contact lifted.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_SCALING_INERTIA

Scaling inertia after contact lifted.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_RAILS_X

Interactions are constrained along the x-axis.

Rails indicate that slight motions off the primary axis of motion are ignored. This makes for a tighter experience for users; when they attempt to pan along a single axis, they are constrained  to the axis.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_RAILS_Y

Interactions are constrained along the y-axis.

Rails indicate that slight motions off the primary axis of motion are ignored. This makes for a tighter experience for users; when they attempt to pan along a single axis, they are constrained  to the axis.


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_EXACT

Report exact distance from initial contact to end of the interaction.

By default, a small distance threshold is subtracted from the first manipulation delta reported by the system. This distance threshold is  intended to account for slight movements of the contact when processing a tap gesture. If this flag is set, the distance threshold is not subtracted from the first delta. 


### -field INTERACTION_CONFIGURATION_FLAG_MANIPULATION_MULTIPLE_FINGER_PANNING


### -field INTERACTION_CONFIGURATION_FLAG_CROSS_SLIDE

All cross-slide interactions enabled.


### -field INTERACTION_CONFIGURATION_FLAG_CROSS_SLIDE_HORIZONTAL

Cross-slide along the x-axis.


### -field INTERACTION_CONFIGURATION_FLAG_CROSS_SLIDE_SELECT

Selection using cross-slide.


### -field INTERACTION_CONFIGURATION_FLAG_CROSS_SLIDE_SPEED_BUMP

Speed bump effect.

A speed bump is a region in which the user experiences a slight drag (or friction) during the swipe or slide gesture.


### -field INTERACTION_CONFIGURATION_FLAG_CROSS_SLIDE_REARRANGE

Rearrange using cross-slide.


### -field INTERACTION_CONFIGURATION_FLAG_CROSS_SLIDE_EXACT

Report exact distance from initial contact to end of the interaction.

By default, a small distance threshold is subtracted from the first cross-slide delta reported by the system. This distance threshold is  intended to account for slight movements of the contact when processing a tap gesture. If this flag is set, the distance threshold is not subtracted from the first delta. 


### -field INTERACTION_CONFIGURATION_FLAG_TAP

Tap.


### -field INTERACTION_CONFIGURATION_FLAG_TAP_DOUBLE

Double tap.


### -field INTERACTION_CONFIGURATION_FLAG_SECONDARY_TAP

Secondary tap.


### -field INTERACTION_CONFIGURATION_FLAG_HOLD

Hold.


### -field INTERACTION_CONFIGURATION_FLAG_HOLD_MOUSE

Hold with mouse.


### -field INTERACTION_CONFIGURATION_FLAG_DRAG

Drag with mouse.


### -field INTERACTION_CONFIGURATION_FLAG_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://msdn.microsoft.com/0cbae801-d6d9-412b-ab8a-0b6c9d7c103e">INTERACTION_CONTEXT_CONFIGURATION</a>



<a href="https://msdn.microsoft.com/0B8D9A5F-F7CF-42B0-A320-77D44445CC24">Interaction Context Enumerations</a>



<a href="https://msdn.microsoft.com/e792e7bc-1c7f-4fa1-810d-97391cbcf797">SetInteractionConfigurationInteractionContext</a>
 

 

