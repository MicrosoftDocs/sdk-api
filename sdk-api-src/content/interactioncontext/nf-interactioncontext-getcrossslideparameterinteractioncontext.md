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

# GetCrossSlideParameterInteractionContext function


## -description


Gets the cross-slide interaction behavior. 


## -parameters




### -param interactionContext [in]

The handle of the interaction context.


### -param threshold [in]

One of the constants from <a href="https://msdn.microsoft.com/c498e2ae-a761-4f93-9ec2-4030b03e64b9">CROSS_SLIDE_THRESHOLD</a>.


### -param distance [out]

The distance threshold of <i>threshold</i>.


## -returns



If this function succeeds, it returns S_OK.
 
Otherwise, it returns an HRESULT error code.




## -see-also




<a href="https://msdn.microsoft.com/3871f24e-34a4-4524-801d-4d60cf6165d9">CROSS_SLIDE_PARAMETER</a>



<a href="https://msdn.microsoft.com/3E3DE99D-B457-4202-8CC2-A6F5C019EFF8">HINTERACTIONCONTEXT</a>



<a href="https://msdn.microsoft.com/0F34F181-D92C-4B08-9F1D-62379D4A2B15">Interaction Context Functions</a>



<a href="https://msdn.microsoft.com/b4d9459a-7b07-4316-bf5c-628de08de7dc">SetCrossSlideParametersInteractionContext</a>
 

 

