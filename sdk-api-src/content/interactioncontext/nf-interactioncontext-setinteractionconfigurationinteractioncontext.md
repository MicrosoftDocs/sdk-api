---
UID: NF:interactioncontext.SetInteractionConfigurationInteractionContext
title: SetInteractionConfigurationInteractionContext function (interactioncontext.h)
description: Configures the Interaction Context object to process the specified manipulations.
helpviewer_keywords: ["SetInteractionConfigurationInteractionContext","SetInteractionConfigurationInteractionContext function","input_intcontext.setinteractionconfigurationinteractioncontext","interactioncontext.setinteractionconfigurationinteractioncontext","interactioncontext/SetInteractionConfigurationInteractionContext"]
old-location: input_intcontext\setinteractionconfigurationinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: e792e7bc-1c7f-4fa1-810d-97391cbcf797
ms.date: 12/05/2018
ms.keywords: SetInteractionConfigurationInteractionContext, SetInteractionConfigurationInteractionContext function, input_intcontext.setinteractionconfigurationinteractioncontext, interactioncontext.setinteractionconfigurationinteractioncontext, interactioncontext/SetInteractionConfigurationInteractionContext
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
req.dll: Ninput.dll; Edgehtml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SetInteractionConfigurationInteractionContext
 - interactioncontext/SetInteractionConfigurationInteractionContext
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ninput.dll
 - edgehtml.dll
 - API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
 - IE_Shims.dll
api_name:
 - SetInteractionConfigurationInteractionContext
---

# SetInteractionConfigurationInteractionContext function


## -description

Configures the <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object to process the specified manipulations.

## -parameters

### -param interactionContext [in]

The handle of the <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.

### -param configurationCount [in]

The number of interactions being configured.

### -param configuration [in]

The interactions to enable for this <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -remarks

By default, no configuration flags are set (no interactions are enabled). Each interaction must be explicitly declared.

Configuration changes are applied only to new interactions.

## -see-also

<a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getinteractionconfigurationinteractioncontext">GetInteractionConfigurationInteractionContext</a>



<a href="/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_context_configuration">INTERACTION_CONTEXT_CONFIGURATION</a>



<a href="/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>