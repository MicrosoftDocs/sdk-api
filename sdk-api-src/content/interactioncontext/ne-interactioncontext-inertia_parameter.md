---
UID: NE:interactioncontext.INERTIA_PARAMETER
title: INERTIA_PARAMETER (interactioncontext.h)
description: Specifies the inertia values for a manipulation (translation, rotation, scaling).
old-location: input_intcontext\inertia_parameter.htm
tech.root: Input_IntContext
ms.assetid: 06a7bab7-3821-42f3-bf2c-2d0724cb1119
ms.date: 12/05/2018
ms.keywords: INERTIA_PARAMETER, INERTIA_PARAMETER enumeration, INERTIA_PARAMETER_EXPANSION_DECELERATION, INERTIA_PARAMETER_EXPANSION_EXPANSION, INERTIA_PARAMETER_MAX, INERTIA_PARAMETER_ROTATION_ANGLE, INERTIA_PARAMETER_ROTATION_DECELERATION, INERTIA_PARAMETER_TRANSLATION_DECELERATION, INERTIA_PARAMETER_TRANSLATION_DISPLACEMENT, input_intcontext.inertia_parameter, interactioncontext.inertia_parameter, interactioncontext/INERTIA_PARAMETER, interactioncontext/INERTIA_PARAMETER_EXPANSION_DECELERATION, interactioncontext/INERTIA_PARAMETER_EXPANSION_EXPANSION, interactioncontext/INERTIA_PARAMETER_MAX, interactioncontext/INERTIA_PARAMETER_ROTATION_ANGLE, interactioncontext/INERTIA_PARAMETER_ROTATION_DECELERATION, interactioncontext/INERTIA_PARAMETER_TRANSLATION_DECELERATION, interactioncontext/INERTIA_PARAMETER_TRANSLATION_DISPLACEMENT
ms.topic: enum
f1_keywords:
- interactioncontext/INERTIA_PARAMETER
dev_langs:
- c++
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
- INERTIA_PARAMETER
targetos: Windows
req.typenames: INERTIA_PARAMETER
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setinertiaparameterinteractioncontext">SetInertiaParameterInteractionContext</a>
 

 

