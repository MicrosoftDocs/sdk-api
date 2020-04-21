---
UID: NF:interactioncontext.AddPointerInteractionContext
title: AddPointerInteractionContext function (interactioncontext.h)
description: Include the specified pointer in the set of pointers processed by the Interaction Context object.helpviewer_keywords: ["AddPointerInteractionContext","AddPointerInteractionContext function","input_intcontext.addpointerinteractioncontext","interactioncontext.addpointerinteractioncontext","interactioncontext/AddPointerInteractionContext"]
old-location: input_intcontext\addpointerinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: a720284f-af50-4e55-ae48-c78a1e826dc4
ms.date: 12/05/2018
ms.keywords: AddPointerInteractionContext, AddPointerInteractionContext function, input_intcontext.addpointerinteractioncontext, interactioncontext.addpointerinteractioncontext, interactioncontext/AddPointerInteractionContext
f1_keywords:
- interactioncontext/AddPointerInteractionContext
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
- AddPointerInteractionContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# AddPointerInteractionContext function


## -description


Include  the specified pointer in the set of pointers processed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object. 


## -parameters




### -param interactionContext [in]

Handle to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object. 


### -param pointerId [in]

ID of the pointer.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



Turn pointer filtering on by setting INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS in <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext">SetPropertyInteractionContext</a>. 




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-getpropertyinteractioncontext">GetPropertyInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-removepointerinteractioncontext">RemovePointerInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext">SetPropertyInteractionContext</a>
 

 

