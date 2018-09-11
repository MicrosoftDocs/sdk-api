---
UID: NF:interactioncontext.DestroyInteractionContext
title: DestroyInteractionContext function
author: windows-sdk-content
description: Destroys the specified Interaction Context object.
old-location: input_intcontext\destroyinteractioncontext.htm
tech.root: Input_IntContext
ms.assetid: 871b35be-ccda-4a74-b516-e1e7f852782d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: DestroyInteractionContext, DestroyInteractionContext function, input_intcontext.destroyinteractioncontext, interactioncontext.destroyinteractioncontext, interactioncontext/DestroyInteractionContext
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
 - DestroyInteractionContext
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DestroyInteractionContext function


## -description


Destroys the specified <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object.


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks



<b>DestroyInteractionContext</b> must be called to destroy any interaction context created by <a href="https://msdn.microsoft.com/90b81d1c-c1c0-442b-a534-f6e39e707230">CreateInteractionContext</a>.




## -see-also




<a href="https://msdn.microsoft.com/90b81d1c-c1c0-442b-a534-f6e39e707230">CreateInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/5c9b7756-fad1-4656-952c-78845685aa21">ResetInteractionContext</a>



<a href="https://msdn.microsoft.com/52fb6054-c8f3-4dbe-af1f-0b8d39ebcf5b">StopInteractionContext</a>
 

 

