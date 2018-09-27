---
UID: NF:interactioncontext.ProcessPointerFramesInteractionContext
title: ProcessPointerFramesInteractionContext function
author: windows-sdk-content
description: Processes a set of pointer input frames.
old-location: input_intcontext\processpointerframesinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 87e70ebf-ff54-4a90-8b28-1cfe6dc33e94
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ProcessPointerFramesInteractionContext, ProcessPointerFramesInteractionContext function, input_intcontext.processpointerframesinteractioncontext, interactioncontext.processpointerframesinteractioncontext, interactioncontext/ProcessPointerFramesInteractionContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
 - ProcessPointerFramesInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ProcessPointerFramesInteractionContext function


## -description


Processes a set of pointer input frames.


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


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


If pointer filtering is set, a sub-frame that includes the specified pointers is extracted from each frame. Pointers are specified through  <a href="https://msdn.microsoft.com/a720284f-af50-4e55-ae48-c78a1e826dc4">AddPointerInteractionContext</a> and pointer filtering turned on by setting INTERACTION_CONTEXT_PROPERTY_FILTER_POINTERS in <a href="https://msdn.microsoft.com/da24831e-9f9f-4a9f-92bf-60e1c5338554">SetPropertyInteractionContext</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

