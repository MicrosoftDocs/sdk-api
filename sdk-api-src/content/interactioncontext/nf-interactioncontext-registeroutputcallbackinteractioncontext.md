---
UID: NF:interactioncontext.RegisterOutputCallbackInteractionContext
title: RegisterOutputCallbackInteractionContext function (interactioncontext.h)
description: Registers a callback to receive interaction events from an Interaction Context object.
helpviewer_keywords: ["RegisterOutputCallbackInteractionContext","RegisterOutputCallbackInteractionContext function","input_intcontext.registeroutputcallbackinteractioncontext","interactioncontext.registeroutputcallbackinteractioncontext","interactioncontext/RegisterOutputCallbackInteractionContext"]
old-location: input_intcontext\registeroutputcallbackinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 87000250-f225-4864-96d2-1e189f5be1a3
ms.date: 12/05/2018
ms.keywords: RegisterOutputCallbackInteractionContext, RegisterOutputCallbackInteractionContext function, input_intcontext.registeroutputcallbackinteractioncontext, interactioncontext.registeroutputcallbackinteractioncontext, interactioncontext/RegisterOutputCallbackInteractionContext
req.header: interactioncontext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RegisterOutputCallbackInteractionContext
 - interactioncontext/RegisterOutputCallbackInteractionContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
 - API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
 - IE_Shims.dll
api_name:
 - RegisterOutputCallbackInteractionContext
---

# RegisterOutputCallbackInteractionContext function

## -description

Registers a callback to receive interaction events from an [Interaction Context](../_input_intcontext/index.md) object.

> [!NOTE]
> See [RegisterOutputCallbackInteractionContext2 function](nf-interactioncontext-registeroutputcallbackinteractioncontext2.md) for enhanced gesture recognition support.

## -parameters

### -param interactionContext [in]

Handle to the [Interaction Context](../_input_intcontext/index.md).

### -param outputCallback [in]

The [INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md).

### -param clientData [in, optional]

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called (**this**).

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

Each instance of an [Interaction Context](../_input_intcontext/index.md) is limited to one output callback. Registering a callback function overwrites any existing callback registration for the Interaction Context.

This function is typically called after the creation of an [Interaction Context](../_input_intcontext/index.md) or when the Interaction Context is reassigned to another UI element.

## -see-also

[INTERACTION_CONTEXT_OUTPUT structure](ns-interactioncontext-interaction_context_output.md)

[INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md)

[INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function](nc-interactioncontext-interaction_context_output_callback.md)

[INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function](nc-interactioncontext-interaction_context_output_callback2.md)
