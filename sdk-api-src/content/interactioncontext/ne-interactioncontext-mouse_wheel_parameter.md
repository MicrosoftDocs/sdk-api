---
UID: NE:interactioncontext.MOUSE_WHEEL_PARAMETER
title: MOUSE_WHEEL_PARAMETER (interactioncontext.h)
description: Specifies the manipulations that can be mapped to mouse wheel rotation.
helpviewer_keywords: ["MOUSE_WHEEL_PARAMETER","MOUSE_WHEEL_PARAMETER enumeration","MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X","MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y","MOUSE_WHEEL_PARAMETER_DELTA_ROTATION","MOUSE_WHEEL_PARAMETER_DELTA_SCALE","MOUSE_WHEEL_PARAMETER_MAX","MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X","MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y","input_intcontext.mouse_wheel_parameter","interactioncontext.mouse_wheel_parameter","interactioncontext/MOUSE_WHEEL_PARAMETER","interactioncontext/MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X","interactioncontext/MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y","interactioncontext/MOUSE_WHEEL_PARAMETER_DELTA_ROTATION","interactioncontext/MOUSE_WHEEL_PARAMETER_DELTA_SCALE","interactioncontext/MOUSE_WHEEL_PARAMETER_MAX","interactioncontext/MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X","interactioncontext/MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y"]
old-location: input_intcontext\mouse_wheel_parameter.htm
tech.root: input_intcontext
ms.assetid: eafc5d3a-f547-45a2-9634-caf309e583f3
ms.date: 12/05/2018
ms.keywords: MOUSE_WHEEL_PARAMETER, MOUSE_WHEEL_PARAMETER enumeration, MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X, MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y, MOUSE_WHEEL_PARAMETER_DELTA_ROTATION, MOUSE_WHEEL_PARAMETER_DELTA_SCALE, MOUSE_WHEEL_PARAMETER_MAX, MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X, MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y, input_intcontext.mouse_wheel_parameter, interactioncontext.mouse_wheel_parameter, interactioncontext/MOUSE_WHEEL_PARAMETER, interactioncontext/MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X, interactioncontext/MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y, interactioncontext/MOUSE_WHEEL_PARAMETER_DELTA_ROTATION, interactioncontext/MOUSE_WHEEL_PARAMETER_DELTA_SCALE, interactioncontext/MOUSE_WHEEL_PARAMETER_MAX, interactioncontext/MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X, interactioncontext/MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y
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
targetos: Windows
req.typenames: MOUSE_WHEEL_PARAMETER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MOUSE_WHEEL_PARAMETER
 - interactioncontext/MOUSE_WHEEL_PARAMETER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - MOUSE_WHEEL_PARAMETER
---

# MOUSE_WHEEL_PARAMETER enumeration


## -description

Specifies the manipulations that can be mapped to mouse wheel rotation.

## -enum-fields

### -field MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_X:0x00000001

Scrolling/panning distance along the x-axis.

### -field MOUSE_WHEEL_PARAMETER_CHAR_TRANSLATION_Y:0x00000002

Scrolling/panning distance along the y-axis.

### -field MOUSE_WHEEL_PARAMETER_DELTA_SCALE:0x00000003

The relative change in scale, as a multiplier, since the last input message.

### -field MOUSE_WHEEL_PARAMETER_DELTA_ROTATION:0x00000004

The relative change in rotation, in radians, since the last input message.

### -field MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_X:0x00000005

Paging distance along the x-axis.

### -field MOUSE_WHEEL_PARAMETER_PAGE_TRANSLATION_Y:0x00000006

Paging distance along the y-axis.

### -field MOUSE_WHEEL_PARAMETER_MAX:0xffffffff

Maximum number of interactions exceeded.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getmousewheelparameterinteractioncontext">GetMouseWheelParameterInteractionContext</a>



<a href="/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setmousewheelparameterinteractioncontext">SetMouseWheelParameterInteractionContext</a>
