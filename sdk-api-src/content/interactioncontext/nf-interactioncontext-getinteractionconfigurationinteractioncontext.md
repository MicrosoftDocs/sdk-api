---
UID: NF:interactioncontext.GetInteractionConfigurationInteractionContext
title: GetInteractionConfigurationInteractionContext function (interactioncontext.h)
description: Gets interaction configuration state for the Interaction Context object.helpviewer_keywords: ["GetInteractionConfigurationInteractionContext","GetInteractionConfigurationInteractionContext function","input_intcontext.getinteractionconfigurationinteractioncontext","interactioncontext.getinteractionconfigurationinteractioncontext","interactioncontext/GetInteractionConfigurationInteractionContext"]
old-location: input_intcontext\getinteractionconfigurationinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 30996835-420a-4141-838f-10b62b562992
ms.date: 12/05/2018
ms.keywords: GetInteractionConfigurationInteractionContext, GetInteractionConfigurationInteractionContext function, input_intcontext.getinteractionconfigurationinteractioncontext, interactioncontext.getinteractionconfigurationinteractioncontext, interactioncontext/GetInteractionConfigurationInteractionContext
f1_keywords:
- interactioncontext/GetInteractionConfigurationInteractionContext
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
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetInteractionConfigurationInteractionContext function


## -description


Gets interaction configuration state  for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.


### -param configurationCount [in]

Number of interaction configurations.


### -param configuration [out]

The interactions enabled for this <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ns-interactioncontext-interaction_context_configuration">INTERACTION_CONTEXT_CONFIGURATION</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setinteractionconfigurationinteractioncontext">SetInteractionConfigurationInteractionContext</a>
 

 

