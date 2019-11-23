---
UID: NF:interactioncontext.ProcessBufferedPacketsInteractionContext
title: ProcessBufferedPacketsInteractionContext function (interactioncontext.h)

description: Process buffered packets at the end of a pointer input frame.
old-location: input_intcontext\processbufferedpacketsinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 52bbeae9-70ab-403c-a035-de2acc2e0599

ms.date: 12/05/2018
ms.keywords: ProcessBufferedPacketsInteractionContext, ProcessBufferedPacketsInteractionContext function, input_intcontext.processbufferedpacketsinteractioncontext, interactioncontext.processbufferedpacketsinteractioncontext, interactioncontext/ProcessBufferedPacketsInteractionContext
ms.topic: function
f1_keywords: 
 - "interactioncontext/ProcessBufferedPacketsInteractionContext"
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
 - ProcessBufferedPacketsInteractionContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ProcessBufferedPacketsInteractionContext function


## -description


Process buffered packets at the end of a pointer input frame.


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



<b>ProcessBufferedPacketsInteractionContext</b> is called at the end of the frame, when the buffer contains all the pointer histories from the frame.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>
 

 

