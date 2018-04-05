---
UID: NF:interactioncontext.SetPropertyInteractionContext
title: SetPropertyInteractionContext function
author: windows-driver-content
description: Sets Interaction Context object properties.
old-location: input_intcontext\setpropertyinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: da24831e-9f9f-4a9f-92bf-60e1c5338554
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: SetPropertyInteractionContext, SetPropertyInteractionContext function, input_intcontext.setpropertyinteractioncontext, interactioncontext.setpropertyinteractioncontext, interactioncontext/SetPropertyInteractionContext
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
-	SetPropertyInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetPropertyInteractionContext function


## -description


Sets <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object properties.


## -parameters




### -param interactionContext [in]

Handle to the <a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> object. 


### -param contextProperty [in]

One of the constants identified by <a href="https://msdn.microsoft.com/b5b96b33-212e-4e1a-89f6-ee9f94de84aa">INTERACTION_CONTEXT_PROPERTY</a>.


### -param value [in]

The value of the constant identified by <i>contextProperty</i>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/a720284f-af50-4e55-ae48-c78a1e826dc4">AddPointerInteractionContext</a>



<a href="https://msdn.microsoft.com/c54a3632-aa7a-416b-b9ed-5ad552403985">GetPropertyInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

