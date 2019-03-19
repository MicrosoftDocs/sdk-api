---
UID: NE:interactioncontext.MOUSE_WHEEL_PARAMETER
title: MOUSE_WHEEL_PARAMETER (interactioncontext.h)
author: windows-sdk-content
description: Specifies the manipulations that can be mapped to mouse wheel rotation.
old-location: input_intcontext\mouse_wheel_parameter.htm
tech.root: Input_IntContext
ms.assetid: eafc5d3a-f547-45a2-9634-caf309e583f3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: MOUSE_WHEEL_PARAMETER, MOUSE_WHEEL_PARAMETER enumeration, MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X, MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y, MOUSE_WHEEL_PARAMETER_DELTA_ROTATION, MOUSE_WHEEL_PARAMETER_DELTA_SCALE, MOUSE_WHEEL_PARAMETER_MAX, MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X, MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y, input_intcontext.mouse_wheel_parameter, interactioncontext.mouse_wheel_parameter, interactioncontext/MOUSE_WHEEL_PARAMETER, interactioncontext/MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X, interactioncontext/MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y, interactioncontext/MOUSE_WHEEL_PARAMETER_DELTA_ROTATION, interactioncontext/MOUSE_WHEEL_PARAMETER_DELTA_SCALE, interactioncontext/MOUSE_WHEEL_PARAMETER_MAX, interactioncontext/MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X, interactioncontext/MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y
ms.topic: enum
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - MOUSE_WHEEL_PARAMETER
product: Windows
targetos: Windows
req.typenames: MOUSE_WHEEL_PARAMETER
req.redist: 
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
 

 

