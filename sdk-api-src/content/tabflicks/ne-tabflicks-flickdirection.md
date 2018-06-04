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

# FLICKDIRECTION enumeration


## -description



Defines the directions in which a pen flick has occurred.




## -enum-fields




### -field FLICKDIRECTION_MIN


### -field FLICKDIRECTION_RIGHT

 A pen flick to the right.


### -field FLICKDIRECTION_UPRIGHT

 A pen flick to the upper right.


### -field FLICKDIRECTION_UP

 An upward pen flick.


### -field FLICKDIRECTION_UPLEFT

A pen flick to the upper left.


### -field FLICKDIRECTION_LEFT

A pen flick to the left.


### -field FLICKDIRECTION_DOWNLEFT

A pen flick to the lower left.


### -field FLICKDIRECTION_DOWN

A downward pen flick.


### -field FLICKDIRECTION_DOWNRIGHT

A pen flick to the down right.


### -field FLICKDIRECTION_INVALID

An invalid pen flick.


## -remarks



A pen flick is a unidirectional pen gesture that requires the user to contact the digitizer in a quick, straight flicking motion. A flick is characterized by high speed and a high degree of straightness. A flick is identified by its direction. Flicks can be made in eight directions corresponding to the cardinal and secondary compass directions.




## -see-also




<a href="https://msdn.microsoft.com/f83994ca-7ebe-42bc-bb54-f101a0a62e52">FLICK_DATA Structure</a>



<a href="https://msdn.microsoft.com/004c7d76-90a9-4506-a70b-dbf8f9e1c616">Flicks Gestures</a>



<a href="https://msdn.microsoft.com/d5c6fa9a-b7a3-4097-bf4f-6d540130f715">Responding to Pen Flicks</a>



<a href="https://msdn.microsoft.com/9433aadf-3440-4249-8f2c-3e22ebc949fb">WM_TABLET_FLICK Message</a>
 

 

