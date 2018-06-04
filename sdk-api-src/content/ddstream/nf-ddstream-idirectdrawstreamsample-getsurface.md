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

# IDirectDrawStreamSample::GetSurface


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
Retrieves pointers to the current sample's DirectDraw surface and associated clipping rectangle.




## -parameters




### -param ppDirectDrawSurface [out]

Address of a pointer to an <b>IDirectDrawSurface</b> interface that specifies the sample's new surface. Set this parameter to <b>NULL</b> if you don't want to specify a new surface.


### -param pRect [out]

Pointer to a <b>RECT</b> structure that will contain the current sample's clipping rectangle. Set this parameter to <b>NULL</b> if you don't want to retrieve the clipping rectangle.


## -returns



Returns an <b>HRESULT</b> value.




## -remarks



Both parameters are optional. All implementations of this interface must support <b>NULL</b> values as valid parameters. If you retrieve a surface pointer, this method increments its reference count, so you must release the reference.




## -see-also




<a href="https://msdn.microsoft.com/afc8ac84-4629-4c5d-b4b2-59c1eb1af35d">IDirectDrawStreamSample Interface</a>
 

 

