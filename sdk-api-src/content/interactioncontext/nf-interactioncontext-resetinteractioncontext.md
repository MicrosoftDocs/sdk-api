---
UID: NF:interactioncontext.ResetInteractionContext
title: ResetInteractionContext function (interactioncontext.h)
description: Resets the interaction state, interaction configuration settings, and all parameters to their initial state. Current interactions are cancelled without notifications. Interaction Context must be reconfigured before next use.helpviewer_keywords: ["ResetInteractionContext","ResetInteractionContext function","input_intcontext.resetinteractioncontext","interactioncontext.resetinteractioncontext","interactioncontext/ResetInteractionContext"]
old-location: input_intcontext\resetinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 5c9b7756-fad1-4656-952c-78845685aa21
ms.date: 12/05/2018
ms.keywords: ResetInteractionContext, ResetInteractionContext function, input_intcontext.resetinteractioncontext, interactioncontext.resetinteractioncontext, interactioncontext/ResetInteractionContext
f1_keywords:
- interactioncontext/ResetInteractionContext
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ResetInteractionContext function


## -description


Resets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_state">interaction state</a>, interaction configuration settings, and all parameters to their initial state.  Current interactions are cancelled without notifications. 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> must be reconfigured before next use.




## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



Useful for managing a pool of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> objects.

Current interactions are cancelled without notifications.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-createinteractioncontext">CreateInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext">DestroyInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-stopinteractioncontext">StopInteractionContext</a>
 

 

