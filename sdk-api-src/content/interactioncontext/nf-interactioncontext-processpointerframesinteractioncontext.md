---
UID: NF:interactioncontext.ProcessPointerFramesInteractionContext
title: ProcessPointerFramesInteractionContext function (interactioncontext.h)
description: Processes a set of pointer input frames.
helpviewer_keywords: ["ProcessPointerFramesInteractionContext","ProcessPointerFramesInteractionContext function","input_intcontext.processpointerframesinteractioncontext","interactioncontext.processpointerframesinteractioncontext","interactioncontext/ProcessPointerFramesInteractionContext"]
old-location: input_intcontext\processpointerframesinteractioncontext.htm
tech.root: input_intcontext
ms.assetid: 87e70ebf-ff54-4a90-8b28-1cfe6dc33e94
ms.date: 12/05/2018
ms.keywords: ProcessPointerFramesInteractionContext, ProcessPointerFramesInteractionContext function, input_intcontext.processpointerframesinteractioncontext, interactioncontext.processpointerframesinteractioncontext, interactioncontext/ProcessPointerFramesInteractionContext
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
 - ProcessPointerFramesInteractionContext
 - interactioncontext/ProcessPointerFramesInteractionContext
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
 - ProcessPointerFramesInteractionContext
---

# ProcessPointerFramesInteractionContext function


## -description

Processes a set of pointer input frames.

## -parameters

### -param interactionContext [in]

Pointer to a handle for the <a href="/previous-versions/windows/desktop/input_intcontext/interaction-context-portal">Interaction Context</a>.

### -param entriesCount [in]

Number of frames to process.

### -param pointerCount [in]

Number of pointers in each frame.

### -param pointerInfo [in]

Pointer to the array of frames (of size <i>entriesCount</i>).

## -returns

If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.

## -remarks

Output notifications are sent as required.

Frames must be processed in reverse chronological order (most recent data first). 

Each frame must have the same set  of input pointers.


Each pointer must originate from a different contact.


If pointer filtering is set, a sub-frame that includes the specified pointers is extracted from each frame. Pointers are specified through  <a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-addpointerinteractioncontext">AddPointerInteractionContext</a> and pointer filtering turned on by setting INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS in <a href="/previous-versions/windows/desktop/api/interactioncontext/nf-interactioncontext-setpropertyinteractioncontext">SetPropertyInteractionContext</a>.

## -see-also

<a href="/previous-versions/windows/desktop/input_intcontext/hinteractioncontext">HINTERACTIONCONTEXT</a>



<a href="/previous-versions/windows/desktop/input_intcontext/functions">Interaction Context Functions</a>