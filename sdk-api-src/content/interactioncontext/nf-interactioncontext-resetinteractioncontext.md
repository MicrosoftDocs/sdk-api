---
UID: NF:interactioncontext.ResetInteractionContext
title: ResetInteractionContext function (interactioncontext.h)
description: Resets the interaction state, interaction configuration settings, and all parameters to their initial state. Current interactions are cancelled without notifications. Interaction Context must be reconfigured before next use.
helpviewer_keywords: ["ResetInteractionContext","ResetInteractionContext function","input_intcontext.resetinteractioncontext","interactioncontext.resetinteractioncontext","interactioncontext/ResetInteractionContext"]
old-location: input_intcontext\resetinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 5c9b7756-fad1-4656-952c-78845685aa21
ms.date: 12/05/2018
ms.keywords: ResetInteractionContext, ResetInteractionContext function, input_intcontext.resetinteractioncontext, interactioncontext.resetinteractioncontext, interactioncontext/ResetInteractionContext
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
 - ResetInteractionContext
 - interactioncontext/ResetInteractionContext
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
 - ResetInteractionContext
---

# ResetInteractionContext function

## -description

Resets the [interaction state](ne-interactioncontext-interaction_state.md), interaction configuration settings, and all parameters to their initial state.  Current interactions are cancelled without notifications.
[Interaction Context](../_input_intcontext/index.md) must be reconfigured before next use.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -remarks

Useful for managing a pool of [Interaction Context](../_input_intcontext/index.md) objects.

Current interactions are cancelled without notifications.

## -see-also

[CreateInteractionContext function](nf-interactioncontext-createinteractioncontext.md)

[DestroyInteractionContext function](nf-interactioncontext-destroyinteractioncontext.md)

[StopInteractionContext function](nf-interactioncontext-stopinteractioncontext.md)
