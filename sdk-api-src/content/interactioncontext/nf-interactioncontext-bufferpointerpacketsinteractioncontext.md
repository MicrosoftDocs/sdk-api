---
UID: NF:interactioncontext.BufferPointerPacketsInteractionContext
title: BufferPointerPacketsInteractionContext function
author: windows-sdk-content
description: Adds the history for a single input pointer to the buffer of the Interaction Context object.
old-location: input_intcontext\bufferpointerpacketsinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: a76c87f9-5811-4a34-9843-f13a0592ddb4
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: BufferPointerPacketsInteractionContext, BufferPointerPacketsInteractionContext function, input_intcontext.bufferpointerpacketsinteractioncontext, interactioncontext.bufferpointerpacketsinteractioncontext, interactioncontext/BufferPointerPacketsInteractionContext
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
req.typenames: MOUSE_WHEEL_PARAMETER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ninput.dll
-	API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
-	IE_Shims.dll
api_name:
-	BufferPointerPacketsInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# BufferPointerPacketsInteractionContext function


## -description


Adds the history for a single input pointer to the buffer of the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


### -param entriesCount [in]

The number of entries in the pointer history.


### -param pointerInfo [in]

Basic pointer information common to all pointer types.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/fee176ba-ad07-4145-0b4d-1b8c335fd102">POINTER_INFO</a>
 

 

