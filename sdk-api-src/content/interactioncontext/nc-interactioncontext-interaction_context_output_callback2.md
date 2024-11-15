---
UID: NC:interactioncontext.INTERACTION_CONTEXT_OUTPUT_CALLBACK2
tech.root: input_intcontext
title: INTERACTION_CONTEXT_OUTPUT_CALLBACK2 (interactioncontext.h)
ms.date: 06/27/2024
description: Callback that receives events from an Interaction Context object.
prerelease: false
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: interactioncontext.h
req.idl: 
req.include-header: 
req.irql: 
targetos: Windows
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 version 21H1
req.target-min-winversvr: Windows Server 2022
req.target-type: Windows
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - LibDef
api_location:
 - interactioncontext.h
api_name:
 - INTERACTION_CONTEXT_OUTPUT_CALLBACK2
f1_keywords:
 - INTERACTION_CONTEXT_OUTPUT_CALLBACK2
 - interactioncontext/INTERACTION_CONTEXT_OUTPUT_CALLBACK2
dev_langs:
 - c++
helpviewer_keywords:
 - INTERACTION_CONTEXT_OUTPUT_CALLBACK2
---

# INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function

## -description

Callback that receives events from an [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param clientData

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called.

### -param output

Output of the [Interaction Context](../_input_intcontext/index.md) object.

## -remarks

Provides enhanced gesture recognition support compared to [INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md).

## -see-also

[INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md)

[INTERACTION_CONTEXT_OUTPUT structure](ns-interactioncontext-interaction_context_output.md)

[INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md)

[INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md)

[RegisterOutputCallbackInteractionContext function](nf-interactioncontext-registeroutputcallbackinteractioncontext.md)

[RegisterOutputCallbackInteractionContext2 function](nf-interactioncontext-registeroutputcallbackinteractioncontext2.md)
