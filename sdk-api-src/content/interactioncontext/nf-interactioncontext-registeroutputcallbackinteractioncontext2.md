---
UID: NF:interactioncontext.RegisterOutputCallbackInteractionContext2
tech.root: input_intcontext
title: RegisterOutputCallbackInteractionContext2
ms.date: 06/28/2024
description: Registers a callback to receive interaction events from an Interaction Context object.
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
req.lib: ninput.lib
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
 - HeaderDef
api_location:
 - interactioncontext.h
api_name:
 - RegisterOutputCallbackInteractionContext2
f1_keywords:
 - RegisterOutputCallbackInteractionContext2
 - interactioncontext/RegisterOutputCallbackInteractionContext2
dev_langs:
 - c++
helpviewer_keywords:
 - RegisterOutputCallbackInteractionContext2
---

# RegisterOutputCallbackInteractionContext2 function

## -description

Registers a callback to receive interaction events from an [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param interactionContext

Handle to the [Interaction Context](../_input_intcontext/index.md).

### -param outputCallback

The [INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function](nc-interactioncontext-interaction_context_output_callback2.md).

### -param clientData

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called (**this**).

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

Provides enhanced gesture recognition support compared to [INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md).

Each instance of an [Interaction Context](../_input_intcontext/index.md) is limited to one output callback. Registering a callback function overwrites any existing callback registration for the Interaction Context.

This function is typically called after the creation of an [Interaction Context](../_input_intcontext/index.md) or when the Interaction Context is reassigned to another UI element.

## -see-also

[INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md)

[INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function](nc-interactioncontext-interaction_context_output_callback2.md)

[INTERACTION_CONTEXT_OUTPUT structure](ns-interactioncontext-interaction_context_output.md)

[INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md)
