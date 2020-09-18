---
UID: NS:interactioncontext.INTERACTION_CONTEXT_OUTPUT
title: INTERACTION_CONTEXT_OUTPUT (interactioncontext.h)
description: Defines the output of the Interaction Context object.
helpviewer_keywords: ["INTERACTION_CONTEXT_OUTPUT","INTERACTION_CONTEXT_OUTPUT structure","input_intcontext.interaction_context_output","interactioncontext.interaction_context_output","interactioncontext/INTERACTION_CONTEXT_OUTPUT"]
old-location: input_intcontext\interaction_context_output.htm
tech.root: input_intcontext
ms.assetid: 90ba531c-9f97-451d-8781-450dbc248f47
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
---

# INTERACTION_CONTEXT_OUTPUT structure


## -description

Defines the output of the  <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.

## -struct-fields

### -field interactionId

ID of the  <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.

### -field interactionFlags

One of the constants from <a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_flags">INTERACTION_FLAGS</a>.

### -field inputType

One of the constants from <a href="/windows/win32/api/winuser/ne-winuser-tagpointer_input_type">POINTER_INPUT_TYPE</a>.

### -field x

The x-coordinate of the input pointer, in HIMETRIC units.

### -field y

The y-coordinate of the input pointer, in HIMETRIC units.

### -field arguments

### -field arguments.manipulation

The state of the manipulation.

### -field arguments.tap

The state of the tap gesture.

### -field arguments.crossSlide

The state of the cross-slide interaction.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_arguments_cross_slide">INTERACTION_ARGUMENTS_CROSS_SLIDE</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_arguments_manipulation">INTERACTION_ARGUMENTS_MANIPULATION</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_arguments_tap">INTERACTION_ARGUMENTS_TAP</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nc-interactioncontext-interaction_context_output_callback">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_flags">INTERACTION_FLAGS</a>



<a href="/previous-versions/windows/desktop/input_intcontext/structures">Interaction Context Structures</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext">RegisterOutputCallbackInteractionContext</a>