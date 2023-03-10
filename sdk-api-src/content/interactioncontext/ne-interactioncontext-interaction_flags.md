---
UID: NE:interactioncontext.INTERACTION_FLAGS
title: INTERACTION_FLAGS (interactioncontext.h)
description: Specifies the state of an interaction.
helpviewer_keywords: ["INTERACTION_FLAGS","INTERACTION_FLAGS enumeration","INTERACTION_FLAG_BEGIN","INTERACTION_FLAG_CANCEL","INTERACTION_FLAG_END","INTERACTION_FLAG_INERTIA","INTERACTION_FLAG_MAX","INTERACTION_FLAG_NONE","input_intcontext.interaction_flags","interactioncontext.interaction_flags","interactioncontext/INTERACTION_FLAGS","interactioncontext/INTERACTION_FLAG_BEGIN","interactioncontext/INTERACTION_FLAG_CANCEL","interactioncontext/INTERACTION_FLAG_END","interactioncontext/INTERACTION_FLAG_INERTIA","interactioncontext/INTERACTION_FLAG_MAX","interactioncontext/INTERACTION_FLAG_NONE"]
old-location: input_intcontext\interaction_flags.htm
tech.root: input_intcontext
ms.assetid: 8d1adbd2-03ca-4609-9738-45bc7b21f934
ms.date: 12/05/2018
ms.keywords: INTERACTION_FLAGS, INTERACTION_FLAGS enumeration, INTERACTION_FLAG_BEGIN, INTERACTION_FLAG_CANCEL, INTERACTION_FLAG_END, INTERACTION_FLAG_INERTIA, INTERACTION_FLAG_MAX, INTERACTION_FLAG_NONE, input_intcontext.interaction_flags, interactioncontext.interaction_flags, interactioncontext/INTERACTION_FLAGS, interactioncontext/INTERACTION_FLAG_BEGIN, interactioncontext/INTERACTION_FLAG_CANCEL, interactioncontext/INTERACTION_FLAG_END, interactioncontext/INTERACTION_FLAG_INERTIA, interactioncontext/INTERACTION_FLAG_MAX, interactioncontext/INTERACTION_FLAG_NONE
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
req.typenames: INTERACTION_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INTERACTION_FLAGS
 - interactioncontext/INTERACTION_FLAGS
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
 - INTERACTION_FLAGS
---

# INTERACTION_FLAGS enumeration


## -description

Specifies the state of an interaction.

## -enum-fields

### -field INTERACTION_FLAG_NONE:0x00000000

No flags set.

### -field INTERACTION_FLAG_BEGIN:0x00000001

The beginning of an interaction.

### -field INTERACTION_FLAG_END:0x00000002

The end of an interaction (including inertia).

### -field INTERACTION_FLAG_CANCEL:0x00000004

Interaction canceled. INTERACTION_FLAG_END also set on cancel.

### -field INTERACTION_FLAG_INERTIA:0x00000008

Inertia being processed.

### -field INTERACTION_FLAG_MAX:0xffffffff

Maximum number of interactions exceeded.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_context_output">INTERACTION_CONTEXT_OUTPUT</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nc-interactioncontext-interaction_context_output_callback">INTERACTION_CONTEXT_OUTPUT_CALLBACK</a>



<a href="/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-registeroutputcallbackinteractioncontext">RegisterOutputCallbackInteractionContext</a>
