---
UID: NF:interactioncontext.CreateInteractionContext
title: CreateInteractionContext function (interactioncontext.h)
author: windows-sdk-content
description: Creates and initializes an Interaction Context object.
old-location: input_intcontext\createinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 90b81d1c-c1c0-442b-a534-f6e39e707230
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateInteractionContext, CreateInteractionContext function, input_intcontext.createinteractioncontext, interactioncontext.createinteractioncontext, interactioncontext/CreateInteractionContext
ms.topic: function
f1_keywords: ["interactioncontext/CreateInteractionContext"]
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
 - CreateInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CreateInteractionContext function


## -description


Creates and initializes an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


## -parameters




### -param interactionContext [out]

Pointer to a handle for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext">DestroyInteractionContext</a> must be called to destroy any interaction context created by <b>CreateInteractionContext</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-destroyinteractioncontext">DestroyInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-resetinteractioncontext">ResetInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-stopinteractioncontext">StopInteractionContext</a>
 

 

