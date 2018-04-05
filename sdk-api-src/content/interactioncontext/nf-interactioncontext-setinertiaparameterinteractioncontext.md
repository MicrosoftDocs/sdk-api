---
UID: NF:interactioncontext.SetInertiaParameterInteractionContext
title: SetInertiaParameterInteractionContext function
author: windows-driver-content
description: Configures the inertia behavior of a manipulation (translation, rotation, scaling) after the contact is lifted.
old-location: input_intcontext\setinertiaparameterinteractioncontext.htm
old-project: Input_IntContext
ms.assetid: 5b228339-3830-407f-a8ea-55f40156cc32
ms.author: windowsdriverdev
ms.date: 3/19/2018
ms.keywords: SetInertiaParameterInteractionContext, SetInertiaParameterInteractionContext function, input_intcontext.setinertiaparameterinteractioncontext, interactioncontext.setinertiaparameterinteractioncontext, interactioncontext/SetInertiaParameterInteractionContext
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
-	SetInertiaParameterInteractionContext
product: Windows
targetos: Windows
req.lib: Ninput.lib
req.dll: Ninput.dll
req.irql: 
req.product: GDI+ 1.1
---

# SetInertiaParameterInteractionContext function


## -description


Configures the inertia behavior of a manipulation (translation, rotation, scaling) after the contact is lifted. 


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


### -param inertiaParameter [in]

One of the constants from <a href="https://msdn.microsoft.com/06a7bab7-3821-42f3-bf2c-2d0724cb1119">INERTIA_PARAMETER</a>.


### -param value [in]

One of the following:

<ul>
<li>The rate of deceleration, in radians/ms².</li>
<li>For translation, the relative change in screen location, in HIMETRIC units.</li>
<li>For rotation, the relative change in angle of rotation, in radianx</li>
<li>For scaling, the relative change in size, in HIMETRIC units.</li>
</ul>

## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -remarks




<a href="https://msdn.microsoft.com/60BFDCD7-D277-4B4A-94DA-7ADB1412252A">Interaction Context</a> uses the inertia system setting for all manipulations (translation, rotation, scaling). This function overrides the system setting.

To restore the system setting, set <i>value</i> to INERTIA_PARAMETER_INVALID_VALUE    FLT_MAX.




## -see-also




<a href="https://msdn.microsoft.com/e3ae71e2-be61-49c1-82a1-2fa82fe9a7ba">GetInertiaParameterInteractionContext</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>
 

 

