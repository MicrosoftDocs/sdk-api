---
UID: NS:interactioncontext.INTERACTION_CONTEXT_CONFIGURATION
title: INTERACTION_CONTEXT_CONFIGURATION
author: windows-sdk-content
description: Defines the configuration of an Interaction Context object that enables, disables, or modifies the behavior of an interaction.
old-location: input_intcontext\interaction_context_configuration.htm
tech.root: Input_IntContext
ms.assetid: 0cbae801-d6d9-412b-ab8a-0b6c9d7c103e
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: INTERACTION_CONTEXT_CONFIGURATION, INTERACTION_CONTEXT_CONFIGURATION structure, input_intcontext.interaction_context_configuration, interactioncontext.interaction_context_configuration, interactioncontext/INTERACTION_CONTEXT_CONFIGURATION
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: INTERACTION_CONTEXT_CONFIGURATION
req.redist: 
---

# INTERACTION_CONTEXT_CONFIGURATION structure


## -description


Defines  the configuration of an <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object that enables, disables, or modifies the behavior of an interaction.


## -struct-fields




### -field interactionId

One of the constants from <a href="https://msdn.microsoft.com/9c6ac9ce-d7c9-4a92-9631-2f241a762525">INTERACTION_ID</a>.

<div class="alert"><b>Note</b>  INTERACTION_FLAG_NONE is not a valid value.</div>
<div> </div>

### -field enable

The value of this property is a bitmask, which can be set to one or more of the values from <a href="https://msdn.microsoft.com/fc26da3a-8769-40c6-a563-1566a46f97f5">INTERACTION_CONFIGURATION_FLAGS</a>.

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




<a href="https://msdn.microsoft.com/38C5CE85-405B-455F-809D-19C77B8A217B">Interaction Context Structures</a>



<a href="https://msdn.microsoft.com/e792e7bc-1c7f-4fa1-810d-97391cbcf797">SetInteractionConfigurationInteractionContext</a>
 

 

