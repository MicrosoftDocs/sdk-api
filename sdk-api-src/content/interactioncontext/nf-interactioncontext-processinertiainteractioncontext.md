---
UID: NF:interactioncontext.ProcessInertiaInteractionContext
title: ProcessInertiaInteractionContext function
author: windows-sdk-content
description: Sends timer input to the Interaction Context object for inertia processing.
old-location: input_intcontext\processinertiainteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: e1f18294-feb2-4340-8ed5-d76600c3d93a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ProcessInertiaInteractionContext, ProcessInertiaInteractionContext function, input_intcontext.processinertiainteractioncontext, interactioncontext.processinertiainteractioncontext, interactioncontext/ProcessInertiaInteractionContext
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
 - ProcessInertiaInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ProcessInertiaInteractionContext function


## -description


Sends timer input to the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object for inertia processing.


## -parameters




### -param interactionContext [in]

Pointer to a handle for the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



The caller is responsible for creating timer when inertia starts, and for driving inertia input with the timer by calling this function from the timer callback. Recommended timer period is 15 ms.



This function has no effect outside inertia.






## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

