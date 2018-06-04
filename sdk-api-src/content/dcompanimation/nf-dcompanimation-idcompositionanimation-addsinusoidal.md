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

# IDCompositionAnimation::AddSinusoidal


## -description


Adds a sinusoidal segment to the animation function.


## -parameters




### -param beginOffset

Type: <b>double</b>

The offset, in seconds, from the beginning of the animation function to the point when this segment should take effect.




### -param bias

Type: <b>float</b>

A constant that is added to the sinusoidal.


### -param amplitude

Type: <b>float</b>

A scale factor that is applied to the sinusoidal.


### -param frequency

Type: <b>float</b>

A scale factor that is applied to the time offset, in Hertz.


### -param phase

Type: <b>float</b>

A constant that is added to the time offset, in degrees.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.




## -remarks



This method fails if any of the parameters are NaN, positive infinity, or negative infinity, or if the <i>beginOffset</i> parameter is negative.



Because animation segments must be added in increasing order, this method fails if the <i>beginOffset</i> parameter is less than or equal to the <i>beginOffset</i> parameter of the previous segment, if any.

This animation segment remains in effect until the begin time of the next segment in the animation function. If the animation function contains no more segments, this segment remains in effect indefinitely. 




## -see-also




<a href="https://msdn.microsoft.com/f914e14b-4ac0-4591-9b7f-6b45b88baaaa">IDCompositionAnimation</a>
 

 

