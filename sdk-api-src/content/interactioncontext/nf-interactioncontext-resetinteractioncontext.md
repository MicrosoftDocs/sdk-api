---
UID: NF:interactioncontext.ResetInteractionContext
title: ResetInteractionContext function
author: windows-sdk-content
description: Resets the interaction state, interaction configuration settings, and all parameters to their initial state. Current interactions are cancelled without notifications. Interaction Context must be reconfigured before next use.
old-location: input_intcontext\resetinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: 5c9b7756-fad1-4656-952c-78845685aa21
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: ResetInteractionContext, ResetInteractionContext function, input_intcontext.resetinteractioncontext, interactioncontext.resetinteractioncontext, interactioncontext/ResetInteractionContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
-	ResetInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# ResetInteractionContext function


## -description


Resets the <a href="https://msdn.microsoft.com/ab44d530-da26-4b40-99d8-f75dd32c3182">interaction state</a>, interaction configuration settings, and all parameters to their initial state.  Current interactions are cancelled without notifications. 
<a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> must be reconfigured before next use.




## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



Useful for managing a pool of <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> objects.

Current interactions are cancelled without notifications.




## -see-also




<a href="https://msdn.microsoft.com/90b81d1c-c1c0-442b-a534-f6e39e707230">CreateInteractionContext</a>



<a href="https://msdn.microsoft.com/871b35be-ccda-4a74-b516-e1e7f852782d">DestroyInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/52fb6054-c8f3-4dbe-af1f-0b8d39ebcf5b">StopInteractionContext</a>
 

 

