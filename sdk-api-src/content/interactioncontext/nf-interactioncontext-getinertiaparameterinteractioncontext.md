---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

