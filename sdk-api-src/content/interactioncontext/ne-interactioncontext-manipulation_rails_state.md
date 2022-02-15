---
UID: NE:interactioncontext.MANIPULATION_RAILS_STATE
title: MANIPULATION_RAILS_STATE (interactioncontext.h)
description: Specifies the rail states for an interaction.
helpviewer_keywords: ["MANIPULATION_RAILS_STATE","MANIPULATION_RAILS_STATE enumeration","MANIPULATION_RAILS_STATE_FREE","MANIPULATION_RAILS_STATE_MAX","MANIPULATION_RAILS_STATE_RAILED","MANIPULATION_RAILS_STATE_UNDECIDED","input_intcontext.manipulation_rails_state","interactioncontext.manipultion_rails_state","interactioncontext/MANIPULATION_RAILS_STATE","interactioncontext/MANIPULATION_RAILS_STATE_FREE","interactioncontext/MANIPULATION_RAILS_STATE_MAX","interactioncontext/MANIPULATION_RAILS_STATE_RAILED","interactioncontext/MANIPULATION_RAILS_STATE_UNDECIDED"]
old-location: input_intcontext\manipulation_rails_state.htm
tech.root: input_intcontext
ms.assetid: b4978408-e124-482e-b552-7a6db76a40ad
ms.date: 12/05/2018
ms.keywords: MANIPULATION_RAILS_STATE, MANIPULATION_RAILS_STATE enumeration, MANIPULATION_RAILS_STATE_FREE, MANIPULATION_RAILS_STATE_MAX, MANIPULATION_RAILS_STATE_RAILED, MANIPULATION_RAILS_STATE_UNDECIDED, input_intcontext.manipulation_rails_state, interactioncontext.manipultion_rails_state, interactioncontext/MANIPULATION_RAILS_STATE, interactioncontext/MANIPULATION_RAILS_STATE_FREE, interactioncontext/MANIPULATION_RAILS_STATE_MAX, interactioncontext/MANIPULATION_RAILS_STATE_RAILED, interactioncontext/MANIPULATION_RAILS_STATE_UNDECIDED
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
req.typenames: MANIPULATION_RAILS_STATE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MANIPULATION_RAILS_STATE
 - interactioncontext/MANIPULATION_RAILS_STATE
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
 - MANIPULATION_RAILS_STATE
---

# MANIPULATION_RAILS_STATE enumeration


## -description

Specifies the rail states for an interaction.

## -enum-fields

### -field MANIPULATION_RAILS_STATE_UNDECIDED:0x00000000

Rail state not defined yet.

### -field MANIPULATION_RAILS_STATE_FREE:0x00000001

Interaction is not constrained to rail.

### -field MANIPULATION_RAILS_STATE_RAILED:0x00000002

Interaction is constrained to rail.

### -field MANIPULATION_RAILS_STATE_MAX:0xffffffff

Maximum number of interactions exceeded.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_arguments_manipulation">INTERACTION_ARGUMENTS_MANIPULATION</a>



<a href="/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext">RegisterOutputCallbackInteractionContext</a>
