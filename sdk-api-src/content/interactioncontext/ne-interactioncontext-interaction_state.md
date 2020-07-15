---
UID: NE:interactioncontext.INTERACTION_STATE
title: INTERACTION_STATE (interactioncontext.h)
description: Specifies the state of the Interaction Context object.
helpviewer_keywords: ["INTERACTION_STATE","INTERACTION_STATE enumeration","INTERACTION_STATE_IDLE","INTERACTION_STATE_IN_INTERACTION","INTERACTION_STATE_MAX","INTERACTION_STATE_POSSIBLE_DOUBLE_TAP","input_intcontext.interaction_state","interactioncontext.interaction_state","interactioncontext/INTERACTION_STATE","interactioncontext/INTERACTION_STATE_IDLE","interactioncontext/INTERACTION_STATE_IN_INTERACTION","interactioncontext/INTERACTION_STATE_MAX","interactioncontext/INTERACTION_STATE_POSSIBLE_DOUBLE_TAP"]
old-location: input_intcontext\interaction_state.htm
tech.root: Input_IntContext
ms.assetid: ab44d530-da26-4b40-99d8-f75dd32c3182
ms.date: 12/05/2018
ms.keywords: INTERACTION_STATE, INTERACTION_STATE enumeration, INTERACTION_STATE_IDLE, INTERACTION_STATE_IN_INTERACTION, INTERACTION_STATE_MAX, INTERACTION_STATE_POSSIBLE_DOUBLE_TAP, input_intcontext.interaction_state, interactioncontext.interaction_state, interactioncontext/INTERACTION_STATE, interactioncontext/INTERACTION_STATE_IDLE, interactioncontext/INTERACTION_STATE_IN_INTERACTION, interactioncontext/INTERACTION_STATE_MAX, interactioncontext/INTERACTION_STATE_POSSIBLE_DOUBLE_TAP
f1_keywords:
- interactioncontext/INTERACTION_STATE
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
- HeaderDef
api_location:
- interactioncontext.h
api_name:
- INTERACTION_STATE
targetos: Windows
req.typenames: INTERACTION_STATE
req.redist: 
ms.custom: 19H1
---

# INTERACTION_STATE enumeration


## -description


Specifies the state of the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


## -enum-fields




### -field INTERACTION_STATE_IDLE

There are no ongoing interactions and all transitional states (inertia, double tap) are complete. It is safe to reuse the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


### -field INTERACTION_STATE_IN_INTERACTION

There is an ongoing interaction. One or more contacts are detected, or inertia is in progress.


### -field INTERACTION_STATE_POSSIBLE_DOUBLE_TAP

All contacts are lifted, but the time threshold for double tap has not been crossed.


### -field INTERACTION_STATE_MAX

Maximum number of interactions exceeded.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getstateinteractioncontext">GetStateInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>
 

 

