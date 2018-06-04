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

# DIRECTMANIPULATION_GESTURE_CONFIGURATION enumeration


## -description


Defines the gestures that can be passed to <a href="https://msdn.microsoft.com/EBBBCEDB-8BAC-4E87-A69C-9730865A257F">SetManualGesture</a>.


## -enum-fields




### -field DIRECTMANIPULATION_GESTURE_NONE

No gestures are defined.


### -field DIRECTMANIPULATION_GESTURE_DEFAULT

Only default gestures are supported. This is the default value.


### -field DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_VERTICAL

Vertical slide and swipe gestures are supported through the cross-slide interaction. For more information, see <a href="https://msdn.microsoft.com/897555e2-c567-4bbe-b600-553daeb223d5">Guidelines for cross-slide</a>.


### -field DIRECTMANIPULATION_GESTURE_CROSS_SLIDE_HORIZONTAL

Horizontal slide and swipe gestures are supported through the cross-slide interaction. For more information, see <a href="https://msdn.microsoft.com/897555e2-c567-4bbe-b600-553daeb223d5">Guidelines for cross-slide</a>.


### -field DIRECTMANIPULATION_GESTURE_PINCH_ZOOM

Pinch and stretch gestures for zooming.


## -remarks



By default, <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> always reassigns tap and press-and-hold gestures to the application. 


Use <b>DIRECTMANIPULATION_GESTURE_PINCH_ZOOM</b> to zoom instead of scale.





## -see-also




<a href="https://msdn.microsoft.com/D116798F-E381-46D4-8271-8BD8CADC9D27">Direct Manipulation Enumerations</a>
 

 

