---
UID: NF:interactioncontext.GetInertiaParameterInteractionContext
title: GetInertiaParameterInteractionContext function
author: windows-sdk-content
description: Gets the inertia behavior of a manipulation (translation, rotation, scaling).
old-location: input_intcontext\getinertiaparameterinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: e3ae71e2-be61-49c1-82a1-2fa82fe9a7ba
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: GetInertiaParameterInteractionContext, GetInertiaParameterInteractionContext function, input_intcontext.getinertiaparameterinteractioncontext, interactioncontext.getinertiaparameterinteractioncontext, interactioncontext/GetInertiaParameterInteractionContext
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
-	GetInertiaParameterInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetInertiaParameterInteractionContext function


## -description


Gets the inertia behavior of a manipulation (translation, rotation, scaling). 


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


### -param inertiaParameter [in]

One of the constants from <a href="https://msdn.microsoft.com/06a7bab7-3821-42f3-bf2c-2d0724cb1119">INERTIA_PARAMETER</a>.


### -param value [out]

The value of <i>inertiaParameter</i>. This value is one of the following:

<ul>
<li>The rate of deceleration, in radians/ms².</li>
<li>For translation, the relative change in screen location, in HIMETRIC units.</li>
<li>For rotation, the relative change in angle of rotation, in radians</li>
<li>For scaling, the relative change in size, in HIMETRIC units.</li>
</ul>

## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/5b228339-3830-407f-a8ea-55f40156cc32">SetInertiaParameterInteractionContext</a>
 

 

