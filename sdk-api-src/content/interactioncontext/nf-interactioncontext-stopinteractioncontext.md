---
UID: NF:interactioncontext.StopInteractionContext
title: StopInteractionContext function
author: windows-sdk-content
description: Sets the interaction state to INTERACTION_STATE_IDLE and leaves all interaction configuration settings and parameters intact.
old-location: input_intcontext\stopinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 52fb6054-c8f3-4dbe-af1f-0b8d39ebcf5b
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: StopInteractionContext, StopInteractionContext function, input_intcontext.stopinteractioncontext, interactioncontext.stopinteractioncontext, interactioncontext/StopInteractionContext
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - StopInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# StopInteractionContext function


## -description


Sets the <a href="https://msdn.microsoft.com/ab44d530-da26-4b40-99d8-f75dd32c3182">interaction state</a> to INTERACTION_STATE_IDLE and leaves all interaction configuration settings and parameters intact. Current interactions are cancelled and notifications sent as required.
<a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> does not have to be reconfigured before next use.




## -parameters




### -param interactionContext [in]

Handle to the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object. 


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/90b81d1c-c1c0-442b-a534-f6e39e707230">CreateInteractionContext</a>



<a href="https://msdn.microsoft.com/871b35be-ccda-4a74-b516-e1e7f852782d">DestroyInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/5c9b7756-fad1-4656-952c-78845685aa21">ResetInteractionContext</a>
 

 

