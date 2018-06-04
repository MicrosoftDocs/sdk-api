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

# MOUSE_WHEEL_PARAMETER enumeration


## -description


Specifies the manipulations that can be mapped to mouse wheel rotation.


## -enum-fields




### -field MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X

Scrolling/panning distance along the x-axis.


### -field MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y

Scrolling/panning distance along the y-axis.


### -field MOUSE_WHEEL_PARAMETER_DELTA_SCALE

The relative change in scale, as a multiplier, since the last input message.


### -field MOUSE_WHEEL_PARAMETER_DELTA_ROTATION

The relative change in rotation, in radians, since the last input message.


### -field MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X

Paging distance along the x-axis.


### -field MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y

Paging distance along the y-axis.


### -field MOUSE_WHEEL_PARAMETER_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://msdn.microsoft.com/2edb742d-a5a1-4c3b-bc0f-c119a2f1c221">GetMouseWheelParameterInteractionContext</a>



<a href="https://msdn.microsoft.com/0B8D9A5F-F7CF-42B0-A320-77D44445CC24">Interaction Context Enumerations</a>



<a href="https://msdn.microsoft.com/fbc47bd4-f78a-4b03-8adc-9b2c4620ea55">SetMouseWheelParameterInteractionContext</a>
 

 

