---
UID: NF:interactioncontext.GetStateInteractionContext
title: GetStateInteractionContext function
author: windows-sdk-content
description: Gets current Interaction Context state and the time when the context will return to idle state.
old-location: input_intcontext\getstateinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: 35d581a9-b1be-4f9b-8783-ccea3469921a
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: GetStateInteractionContext, GetStateInteractionContext function, input_intcontext.getstateinteractioncontext, interactioncontext.getstateinteractioncontext, interactioncontext/GetStateInteractionContext
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	ninput.dll
-	API-MS-Win-Input-IE-InteractionContext-l1-1-0.dll
-	IE_Shims.dll
api_name:
-	GetStateInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetStateInteractionContext function


## -description


Gets current <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> state and the time when the context will return to idle state. 


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


### -param pointerInfo [in]

Basic pointer information common to all pointer types.


### -param state [out]

One of the constants from <a href="https://msdn.microsoft.com/ab44d530-da26-4b40-99d8-f75dd32c3182">INTERACTION_STATE</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



After interaction ends, the interaction context might still be busy reporting inertia, or expecting second tap in a double tap gesture (in general, if multi-stroke gesture is possible). This function allows the caller to find out when it is safe to treat the Interaction Context object as idle. The main purpose of this function is management of pools of interaction contexts.




## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

