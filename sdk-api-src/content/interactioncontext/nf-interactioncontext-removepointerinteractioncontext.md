---
UID: NF:interactioncontext.RemovePointerInteractionContext
title: RemovePointerInteractionContext function (interactioncontext.h)
author: windows-sdk-content
description: Remove the specified pointer from the set of pointers processed by the Interaction Context object.
old-location: input_intcontext\removepointerinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: d17f329b-f633-4aec-806f-3643206fce29
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RemovePointerInteractionContext, RemovePointerInteractionContext function, input_intcontext.removepointerinteractioncontext, interactioncontext.removepointerinteractioncontext, interactioncontext/RemovePointerInteractionContext
ms.topic: function
f1_keywords: 
 - "interactioncontext/RemovePointerInteractionContext"
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
 - RemovePointerInteractionContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RemovePointerInteractionContext function


## -description


Remove  the specified pointer from the set of pointers processed by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object. 


## -parameters




### -param interactionContext [in]

Handle to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a> object. 


### -param pointerId [in]

ID of the pointer.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext">AddPointerInteractionContext</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>
 

 

