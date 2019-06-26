---
UID: NF:interactioncontext.DestroyInteractionContext
title: DestroyInteractionContext function (interactioncontext.h)
author: windows-sdk-content
description: Destroys the specified Interaction Context object.
old-location: input_intcontext\destroyinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 871b35be-ccda-4a74-b516-e1e7f852782d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DestroyInteractionContext, DestroyInteractionContext function, input_intcontext.destroyinteractioncontext, interactioncontext.destroyinteractioncontext, interactioncontext/DestroyInteractionContext
ms.topic: function
f1_keywords: 
 - "interactioncontext/DestroyInteractionContext"
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
 - DestroyInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DestroyInteractionContext function


## -description


Destroys the specified <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object.


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



<b>DestroyInteractionContext</b> must be called to destroy any interaction context created by <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-createinteractioncontext">CreateInteractionContext</a>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-createinteractioncontext">CreateInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-resetinteractioncontext">ResetInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-stopinteractioncontext">StopInteractionContext</a>
 

 

