---
UID: NS:interactioncontext.INTERACTION_ARGUMENTS_MANIPULATION
title: INTERACTION_ARGUMENTS_MANIPULATION (interactioncontext.h)
description: Defines the state of a manipulation.
helpviewer_keywords: ["INTERACTION_ARGUMENTS_MANIPULATION","INTERACTION_ARGUMENTS_MANIPULATION structure","input_intcontext.interaction_arguments_manipulation","interactioncontext.interaction_arguments_manipulation","interactioncontext/INTERACTION_ARGUMENTS_MANIPULATION"]
old-location: input_intcontext\interaction_arguments_manipulation.htm
tech.root: input_intcontext
ms.assetid: 8ef21f5a-51ae-4923-a5b4-0ee18bca563f
ms.date: 12/05/2018
ms.keywords: INTERACTION_ARGUMENTS_MANIPULATION, INTERACTION_ARGUMENTS_MANIPULATION structure, input_intcontext.interaction_arguments_manipulation, interactioncontext.interaction_arguments_manipulation, interactioncontext/INTERACTION_ARGUMENTS_MANIPULATION
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
req.typenames: INTERACTION_ARGUMENTS_MANIPULATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERACTION_ARGUMENTS_MANIPULATION
 - interactioncontext/INTERACTION_ARGUMENTS_MANIPULATION
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
 - INTERACTION_ARGUMENTS_MANIPULATION
---

# INTERACTION_ARGUMENTS_MANIPULATION structure

## -description

Defines  the state of a manipulation.

## -struct-fields

### -field delta

The change in translation, rotation, and scale since the last [INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md).

### -field cumulative

The accumulated change in translation, rotation, and scale since the interaction started.

### -field velocity

The velocities of the accumulated transformations for the interaction.

### -field railsState

One of the constants from [MANIPULATION_RAILS_STATE enumeration](ne-interactioncontext-manipulation_rails_state.md).

## -see-also

[INTERACTION_CONTEXT_OUTPUT structure](ns-interactioncontext-interaction_context_output.md)

[INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md)

[RegisterOutputCallbackInteractionContext function](nf-interactioncontext-registeroutputcallbackinteractioncontext.md)

[RegisterOutputCallbackInteractionContext2 function](nf-interactioncontext-registeroutputcallbackinteractioncontext2.md)
