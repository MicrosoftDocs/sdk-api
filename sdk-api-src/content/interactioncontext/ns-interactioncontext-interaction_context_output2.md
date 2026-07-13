---
UID: NS:interactioncontext.INTERACTION_CONTEXT_OUTPUT2
title: INTERACTION_CONTEXT_OUTPUT2
description: Defines the output of the Interaction Context object.
tech.root: input_intcontext
ms.date: 06/28/2024
ms.keywords: INTERACTION_CONTEXT_OUTPUT2, INTERACTION_CONTEXT_OUTPUT2 structure, input_intcontext.interaction_context_output2, interactioncontext.interaction_context_output2, interactioncontext/INTERACTION_CONTEXT_OUTPUT2
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 version 21H1
req.target-min-winversvr: Windows Server 2022
req.kmdf-ver: 
req.ddi-compliance: 
req.dll: 
req.lib: 
req.max-support: 
req.redist: 
req.typenames: INTERACTION_CONTEXT_OUTPUT2
typedef_isUnnamed: false
req.umdf-ver: 
req.unicode-ansi: 
req.construct-type: structure
targetos: Windows
topic_type:
 - apiref
api_type:
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - INTERACTION_CONTEXT_OUTPUT2
f1_keywords:
 - INTERACTION_CONTEXT_OUTPUT2
 - interactioncontext/INTERACTION_CONTEXT_OUTPUT2
dev_langs:
 - c++
helpviewer_keywords:
 - INTERACTION_CONTEXT_OUTPUT2
---

# INTERACTION_CONTEXT_OUTPUT2 structure

## -description

Defines the output of the [Interaction Context](../_input_intcontext/index.md) object.

## -struct-fields

### -field interactionId

ID of the  [Interaction Context](../_input_intcontext/index.md) object.

### -field interactionFlags

One of the constants from [INTERACTION_FLAGS enumeration](ne-interactioncontext-interaction_flags.md).

### -field inputType

One of the constants from [POINTER_INPUT_TYPE enumeration](../winuser/ne-winuser-tagpointer_input_type.md).

### -field contactCount

The number of contacts that can be recognized.

### -field currentContactCount

The number of current contacts.

### -field x

The x-coordinate of the input pointer, in HIMETRIC units.

### -field y

The y-coordinate of the input pointer, in HIMETRIC units.

### -field arguments

Union of *arguments* sub-fields.

### -field arguments.manipulation

The state of the manipulation.

### -field arguments.tap

The state of the tap gesture.

### -field arguments.crossSlide

The state of the cross-slide interaction.

## -remarks

Provides enhanced gesture recognition support compared to the [INTERACTION_CONTEXT_OUTPUT structure](ns-interactioncontext-interaction_context_output.md).

## -see-also

[INTERACTION_ARGUMENTS_CROSS_SLIDE structure](ns-interactioncontext-interaction_arguments_cross_slide.md)

[INTERACTION_ARGUMENTS_MANIPULATION structure](ns-interactioncontext-interaction_arguments_manipulation.md)

[INTERACTION_ARGUMENTS_TAP structure](ns-interactioncontext-interaction_arguments_tap.md)

[INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md)

[INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function](nc-interactioncontext-interaction_context_output_callback2.md)

[INTERACTION_FLAGS enumeration](ne-interactioncontext-interaction_flags.md)

[RegisterOutputCallbackInteractionContext function](nf-interactioncontext-registeroutputcallbackinteractioncontext.md)

[RegisterOutputCallbackInteractionContext2 function](nf-interactioncontext-registeroutputcallbackinteractioncontext2.md)
