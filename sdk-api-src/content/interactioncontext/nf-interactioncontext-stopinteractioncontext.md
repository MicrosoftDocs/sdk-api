---
UID: NF:interactioncontext.StopInteractionContext
title: StopInteractionContext function (interactioncontext.h)
author: windows-sdk-content
description: Sets the interaction state to INTERACTION_STATE_IDLE and leaves all interaction configuration settings and parameters intact.
old-location: input_intcontext\stopinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 52fb6054-c8f3-4dbe-af1f-0b8d39ebcf5b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: StopInteractionContext, StopInteractionContext function, input_intcontext.stopinteractioncontext, interactioncontext.stopinteractioncontext, interactioncontext/StopInteractionContext
ms.topic: function
f1_keywords: 
 - "interactioncontext/StopInteractionContext"
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
 - StopInteractionContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# StopInteractionContext function


## -description


Sets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/ne-interactioncontext-interaction_state">interaction state</a> to INTERACTION_STATE_IDLE and leaves all interaction configuration settings and parameters intact. Current interactions are cancelled and notifications sent as required.
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> does not have to be reconfigured before next use.




## -parameters




### -param interactionContext [in]

Handle to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object. 


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-createinteractioncontext">CreateInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext">DestroyInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-resetinteractioncontext">ResetInteractionContext</a>
 

 

