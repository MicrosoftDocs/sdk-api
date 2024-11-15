---
UID: NF:interactioncontext.GetInteractionConfigurationInteractionContext
title: GetInteractionConfigurationInteractionContext function (interactioncontext.h)
description: Gets interaction configuration state for the Interaction Context object.
helpviewer_keywords: ["GetInteractionConfigurationInteractionContext","GetInteractionConfigurationInteractionContext function","input_intcontext.getinteractionconfigurationinteractioncontext","interactioncontext.getinteractionconfigurationinteractioncontext","interactioncontext/GetInteractionConfigurationInteractionContext"]
old-location: input_intcontext\getinteractionconfigurationinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 30996835-420a-4141-838f-10b62b562992
ms.date: 12/05/2018
ms.keywords: GetInteractionConfigurationInteractionContext, GetInteractionConfigurationInteractionContext function, input_intcontext.getinteractionconfigurationinteractioncontext, interactioncontext.getinteractionconfigurationinteractioncontext, interactioncontext/GetInteractionConfigurationInteractionContext
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
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetInteractionConfigurationInteractionContext
 - interactioncontext/GetInteractionConfigurationInteractionContext
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
 - GetInteractionConfigurationInteractionContext
---

# GetInteractionConfigurationInteractionContext function

## -description

Gets interaction configuration state  for the [Interaction Context](../_input_intcontext/index.md) object.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the [Interaction Context](../_input_intcontext/index.md).

### -param configurationCount [in]

Number of interaction configurations.

### -param configuration [out]

The interactions enabled for this [Interaction Context](../_input_intcontext/index.md) object.

## -returns

If this function succeeds, it returns S_OK.

Otherwise, it returns an HRESULT error code.

## -see-also

[INTERACTION_CONTEXT_CONFIGURATION structure](ns-interactioncontext-interaction_context_configuration.md)

[SetInteractionConfigurationInteractionContext function](nf-interactioncontext-setinteractionconfigurationinteractioncontext.md)
