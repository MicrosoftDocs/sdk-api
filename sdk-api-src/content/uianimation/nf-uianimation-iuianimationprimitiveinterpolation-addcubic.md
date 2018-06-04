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

# IUIAnimationPrimitiveInterpolation::AddCubic


## -description


Adds a cubic polynomial segment that describes the shape of a transition curve to the animation function.


## -parameters




### -param dimension




### -param beginOffset [in]

The begin offset for the segment, where 0 corresponds to the start of the transition.


### -param constantCoefficient [in]

The cubic polynomial constant coefficient.


### -param linearCoefficient [in]

The cubic polynomial linear coefficient.


### -param quadraticCoefficient [in]

The cubic polynomial quadratic coefficient.


### -param cubicCoefficient [in]

The cubic polynomial cubic coefficient.


#### - cDimension [in]

The dimension in which to apply the new segment.


## -returns



If this method succeeds, it returns S_OK. Otherwise, it returns an  <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/38f15d61-d415-4c7d-b454-5144fc7c9b1e">Windows Animation Error Codes</a> for a list of error codes.




## -remarks



This method will fail with an error code of UI_E_INVALID_PRIMITIVE if the start time is either less than 0
or less than the start time of  a previous segment.





## -see-also




<a href="https://msdn.microsoft.com/6EAE7874-1103-4D2E-A325-37E5A95705F5">IUIAnimationPrimitiveInterpolation</a>
 

 

