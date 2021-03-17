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

Registers a callback to receive interaction events from an <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.

## -parameters

### -param interactionContext [in]

Handle to the <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.

### -param outputCallback [in]

The callback function.

### -param clientData [in, optional]

A pointer to an object that contains information about the client. The value typically points to the object for which the member function is called (<b>this</b>).

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -remarks

Each instance of an <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> is limited to one output callback. Registering a callback function overwrites any existing callback registration for the Interaction Context.

This function is typically called after the creation of an <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> or when the Interaction Context is reassigned to another UI element.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_context_output">INTERACTION_CONTEXT_OUTPUT</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nc-interactioncontext-interaction_context_output_callback">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>



<a href="/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>