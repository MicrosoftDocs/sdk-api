---
UID: NC:interactioncontext.INTERACTION_CONTEXT_OUTPUT_CALLBACK
title: INTERACTION_CONTEXT_OUTPUT_CALLBACK (interactioncontext.h)
description: Callback that receives events from an Interaction Context object.
helpviewer_keywords: ["INTERACTION_CONTEXT_OUTPUT_CALLBACK","INTERACTION_CONTEXT_OUTPUT_CALLBACK callback","INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function","input_intcontext.interaction_context_output_callback","interactioncontext.interaction_context_output_callback","interactioncontext/INTERACTION_CONTEXT_OUTPUT_CALLBACK"]
old-location: input_intcontext\interaction_context_output_callback.htm
tech.root: input_intcontext
ms.assetid: 7d2badad-5b98-4717-9409-5ee75d8fa213
ms.date: 12/05/2018
ms.keywords: INTERACTION_CONTEXT_OUTPUT_CALLBACK, INTERACTION_CONTEXT_OUTPUT_CALLBACK callback, INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function, input_intcontext.interaction_context_output_callback, interactioncontext.interaction_context_output_callback, interactioncontext/INTERACTION_CONTEXT_OUTPUT_CALLBACK
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERACTION_CONTEXT_OUTPUT_CALLBACK
 - interactioncontext/INTERACTION_CONTEXT_OUTPUT_CALLBACK
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - interactioncontext.h
api_name:
 - INTERACTION_CONTEXT_OUTPUT_CALLBACK
---

# INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function

## -description

Callback that receives events from an [Interaction Context](../_input_intcontext/index.md) object.

> [!NOTE]
> See [INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function](nc-interactioncontext-interaction_context_output_callback2.md) for enhanced gesture recognition support.

## -parameters

### -param clientData [in, optional]

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called.

### -param output [in]

Output of the [Interaction Context](../_input_intcontext/index.md) object.

## -see-also

[INTERACTION_CONTEXT_OUTPUT_CALLBACK2 callback function](nc-interactioncontext-interaction_context_output_callback2.md)

[INTERACTION_CONTEXT_OUTPUT structure](ns-interactioncontext-interaction_context_output.md)

[INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md)

[INTERACTION_CONTEXT_OUTPUT2 structure](ns-interactioncontext-interaction_context_output2.md)

[RegisterOutputCallbackInteractionContext function](nf-interactioncontext-registeroutputcallbackinteractioncontext.md)

[RegisterOutputCallbackInteractionContext2 function](nf-interactioncontext-registeroutputcallbackinteractioncontext2.md)
