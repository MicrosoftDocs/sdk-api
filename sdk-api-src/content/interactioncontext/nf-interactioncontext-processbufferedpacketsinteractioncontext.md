---
UID: NF:interactioncontext.ProcessBufferedPacketsInteractionContext
title: ProcessBufferedPacketsInteractionContext function
author: windows-sdk-content
description: Process buffered packets at the end of a pointer input frame.
old-location: input_intcontext\processbufferedpacketsinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: 52bbeae9-70ab-403c-a035-de2acc2e0599
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ProcessBufferedPacketsInteractionContext, ProcessBufferedPacketsInteractionContext function, input_intcontext.processbufferedpacketsinteractioncontext, interactioncontext.processbufferedpacketsinteractioncontext, interactioncontext/ProcessBufferedPacketsInteractionContext
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MOUSE_WHEEL_PARAMETER
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
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# ProcessBufferedPacketsInteractionContext function


## -description


Process buffered packets at the end of a pointer input frame.


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



<b>ProcessBufferedPacketsInteractionContext</b> is called at the end of the frame, when the buffer contains all the pointer histories from the frame.




## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

