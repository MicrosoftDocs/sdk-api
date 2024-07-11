---
UID: NS:interactioncontext.INTERACTION_CONTEXT_OUTPUT
title: INTERACTION_CONTEXT_OUTPUT (interactioncontext.h)
description: Defines the output of the Interaction Context object.
tech.root: input_intcontext
ms.date: 12/05/2018
ms.keywords: INTERACTION_CONTEXT_OUTPUT, INTERACTION_CONTEXT_OUTPUT structure, input_intcontext.interaction_context_output, interactioncontext.interaction_context_output, interactioncontext/INTERACTION_CONTEXT_OUTPUT
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
req.typenames: INTERACTION_CONTEXT_OUTPUT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERACTION_CONTEXT_OUTPUT
 - interactioncontext/INTERACTION_CONTEXT_OUTPUT
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
 - INTERACTION_CONTEXT_OUTPUT
helpviewer_keywords: ["INTERACTION_CONTEXT_OUTPUT","INTERACTION_CONTEXT_OUTPUT structure","input_intcontext.interaction_context_output","interactioncontext.interaction_context_output","interactioncontext/INTERACTION_CONTEXT_OUTPUT"]
---

# INTERACTION_CONTEXT_OUTPUT structure

## -description

Defines the output of the  [Interaction Context](../_input_intcontext/index.md) object.

> [!NOTE]
> See [INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md) for enhanced gesture recognition support.

## -struct-fields

### -field interactionId

ID of the  [Interaction Context](../_input_intcontext/index.md) object.

### -field interactionFlags

One of the constants from [INTERACTION_FLAGS enumeration](ne-interactioncontext-interaction_flags.md).

### -field inputType

One of the constants from [POINTER_INPUT_TYPE enumeration](../winuser/ne-winuser-tagpointer_input_type.md).

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

## -see-also

[INTERACTION_ARGUMENTS_CROSS_SLIDE structure](ns-interactioncontext-interaction_arguments_cross_slide.md)

[INTERACTION_ARGUMENTS_MANIPULATION structure](ns-interactioncontext-interaction_arguments_manipulation.md)

[INTERACTION_ARGUMENTS_TAP structure](ns-interactioncontext-interaction_arguments_tap.md)

[INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md)

[INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function](nc-interactioncontext-interaction_context_output_callback2.md)

[INTERACTION_FLAGS enumeration](ne-interactioncontext-interaction_flags.md)

[RegisterOutputCallbackInteractionContext function](nf-interactioncontext-registeroutputcallbackinteractioncontext.md)

[RegisterOutputCallbackInteractionContext2 function](nf-interactioncontext-registeroutputcallbackinteractioncontext2.md)
