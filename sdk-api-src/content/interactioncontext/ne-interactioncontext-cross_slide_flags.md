---
UID: NE:interactioncontext.CROSS_SLIDE_FLAGS
title: CROSS_SLIDE_FLAGS (interactioncontext.h)
description: Specifies the state of the cross-slide interaction.
helpviewer_keywords: ["CROSS_SLIDE_FLAGS","CROSS_SLIDE_FLAGS enumeration","CROSS_SLIDE_FLAGS_MAX","CROSS_SLIDE_FLAGS_NONE","CROSS_SLIDE_FLAGS_REARRANGE","CROSS_SLIDE_FLAGS_SELECT","CROSS_SLIDE_FLAGS_SPEED_BUMP","input_intcontext.cross_slide_flags","interactioncontext.cross_slide_flags","interactioncontext/CROSS_SLIDE_FLAGS","interactioncontext/CROSS_SLIDE_FLAGS_MAX","interactioncontext/CROSS_SLIDE_FLAGS_NONE","interactioncontext/CROSS_SLIDE_FLAGS_REARRANGE","interactioncontext/CROSS_SLIDE_FLAGS_SELECT","interactioncontext/CROSS_SLIDE_FLAGS_SPEED_BUMP"]
old-location: input_intcontext\cross_slide_flags.htm
tech.root: input_intcontext
ms.assetid: 3be72ad1-87da-4c08-84fd-a84d4c03d33b
ms.date: 12/05/2018
ms.keywords: CROSS_SLIDE_FLAGS, CROSS_SLIDE_FLAGS enumeration, CROSS_SLIDE_FLAGS_MAX, CROSS_SLIDE_FLAGS_NONE, CROSS_SLIDE_FLAGS_REARRANGE, CROSS_SLIDE_FLAGS_SELECT, CROSS_SLIDE_FLAGS_SPEED_BUMP, input_intcontext.cross_slide_flags, interactioncontext.cross_slide_flags, interactioncontext/CROSS_SLIDE_FLAGS, interactioncontext/CROSS_SLIDE_FLAGS_MAX, interactioncontext/CROSS_SLIDE_FLAGS_NONE, interactioncontext/CROSS_SLIDE_FLAGS_REARRANGE, interactioncontext/CROSS_SLIDE_FLAGS_SELECT, interactioncontext/CROSS_SLIDE_FLAGS_SPEED_BUMP
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
req.typenames: CROSS_SLIDE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CROSS_SLIDE_FLAGS
 - interactioncontext/CROSS_SLIDE_FLAGS
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
 - CROSS_SLIDE_FLAGS
---

# CROSS_SLIDE_FLAGS enumeration


## -description

Specifies the state of the cross-slide interaction.

## -enum-fields

### -field CROSS_SLIDE_FLAGS_NONE:0x00000000

No cross-slide interaction.

### -field CROSS_SLIDE_FLAGS_SELECT:0x00000001

Cross-slide interaction has crossed a distance threshold and is in select mode.

### -field CROSS_SLIDE_FLAGS_SPEED_BUMP:0x00000002

Cross-slide interaction is in speed bump mode.

### -field CROSS_SLIDE_FLAGS_REARRANGE:0x00000004

Cross-slide interaction has crossed the speed bump threshold and is in rearrange (drag and drop) mode.

### -field CROSS_SLIDE_FLAGS_MAX:0xffffffff

Maximum number of interactions exceeded.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_arguments_cross_slide">INTERACTION_ARGUMENTS_CROSS_SLIDE</a>



<a href="/previous-versions/windows/desktop/input_intcontext/enumerations">Interaction Context Enumerations</a>
