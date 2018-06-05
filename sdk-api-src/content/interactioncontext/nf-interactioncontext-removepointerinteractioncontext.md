---
UID: NF:interactioncontext.RemovePointerInteractionContext
title: RemovePointerInteractionContext function
author: windows-sdk-content
description: Remove the specified pointer from the set of pointers processed by the Interaction Context object.
old-location: input_intcontext\removepointerinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: d17f329b-f633-4aec-806f-3643206fce29
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: RemovePointerInteractionContext, RemovePointerInteractionContext function, input_intcontext.removepointerinteractioncontext, interactioncontext.removepointerinteractioncontext, interactioncontext/RemovePointerInteractionContext
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
-	RemovePointerInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# RemovePointerInteractionContext function


## -description


Remove  the specified pointer from the set of pointers processed by the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object. 


## -parameters




### -param interactionContext [in]

Handle to the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object. 


### -param pointerId [in]

ID of the pointer.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/a720284f-af50-4e55-ae48-c78a1e826dc4">AddPointerInteractionContext</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

