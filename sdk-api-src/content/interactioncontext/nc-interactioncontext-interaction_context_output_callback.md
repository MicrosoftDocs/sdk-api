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
f1_keywords:
- interactioncontext/INTERACTION_CONTEXT_OUTPUT_CALLBACK
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
- UserDefined
api_location:
- interactioncontext.h
api_name:
- INTERACTION_CONTEXT_OUTPUT_CALLBACK
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# INTERACTION_CONTEXT_OUTPUT_CALLBACK callback function


## -description


Callback that receives events from an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


## -parameters




### -param *clientData [in, optional]

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called.


### -param *output [in]

Output of the  <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_context_output">INTERACTION_CONTEXT_OUTPUT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-reference">Interaction Context Reference</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext">RegisterOutputCallbackInteractionContext</a>
 

 

