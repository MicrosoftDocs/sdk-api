---
UID: NS:interactioncontext.INTERACTION_CONTEXT_CONFIGURATION
title: INTERACTION_CONTEXT_CONFIGURATION (interactioncontext.h)
description: Defines the configuration of an Interaction Context object that enables, disables, or modifies the behavior of an interaction.
helpviewer_keywords: ["INTERACTION_CONTEXT_CONFIGURATION","INTERACTION_CONTEXT_CONFIGURATION structure","input_intcontext.interaction_context_configuration","interactioncontext.interaction_context_configuration","interactioncontext/INTERACTION_CONTEXT_CONFIGURATION"]
old-location: input_intcontext\interaction_context_configuration.htm
tech.root: input_intcontext
ms.assetid: 0cbae801-d6d9-412b-ab8a-0b6c9d7c103e
ms.date: 12/05/2018
ms.keywords: INTERACTION_CONTEXT_CONFIGURATION, INTERACTION_CONTEXT_CONFIGURATION structure, input_intcontext.interaction_context_configuration, interactioncontext.interaction_context_configuration, interactioncontext/INTERACTION_CONTEXT_CONFIGURATION
f1_keywords:
- interactioncontext/INTERACTION_CONTEXT_CONFIGURATION
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
- INTERACTION_CONTEXT_CONFIGURATION
targetos: Windows
req.typenames: INTERACTION_CONTEXT_CONFIGURATION
req.redist: 
ms.custom: 19H1
---

# INTERACTION_CONTEXT_CONFIGURATION structure


## -description


Defines  the configuration of an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object that enables, disables, or modifies the behavior of an interaction.


## -struct-fields




### -field interactionId

One of the constants from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_id">INTERACTION_ID</a>.

<div class="alert"><b>Note</b>  INTERACTION_FLAG_NONE is not a valid value.</div>
<div> </div>

### -field enable

The value of this property is a bitmask, which can be set to one or more of the values from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_configuration_flags">INTERACTION_CONFIGURATION_FLAGS</a>.

This example shows the default setting for <b>INTERACTION_CONTEXT_CONFIGURATION</b>.


```cpp
#define INTERACTION_CONTEXT_CONFIGURATION_DEFAULT                         \
{                                                                         \
    {INTERACTION_ID_MANIPULATION,                                         \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION |                     \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION_TRANSLATION_X |       \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION_TRANSLATION_Y |       \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION_ROTATION |            \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION_SCALING |             \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION_TRANSLATION_INERTIA | \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION_ROTATION_INERTIA |    \
        INTERACTION_CONFIGURATION_FLAG_MANIPULATION_SCALING_INERTIA},     \
    {INTERACTION_ID_TAP,                                                  \
        INTERACTION_CONFIGURATION_FLAG_TAP},                              \
    {INTERACTION_ID_SECONDARY_TAP,                                        \
        INTERACTION_CONFIGURATION_FLAG_SECONDARY_TAP},                    \
    {INTERACTION_ID_HOLD,                                                 \
        INTERACTION_CONFIGURATION_FLAG_HOLD},                             \
    {INTERACTION_ID_DRAG,                                                 \
        INTERACTION_CONFIGURATION_FLAG_NONE},                             \
    {INTERACTION_ID_CROSS_SLIDE,                                          \
        INTERACTION_CONFIGURATION_FLAG_NONE}                              \
}                                                                         \
```



## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/structures">Interaction Context Structures</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext">SetInteractionConfigurationInteractionContext</a>
 

 

