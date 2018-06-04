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

# IDirectManipulationViewport2::RemoveBehavior


## -description


Removes a behavior from the viewport that matches the given cookie.


## -parameters




### -param cookie [in]

A valid cookie returned from the <a href="https://msdn.microsoft.com/E65CF2A3-EF44-4B4E-A8C5-7DC75345B5A6">AddBehavior</a> call on the same viewport.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. If the behavior has already been removed or if the behavior is not attached to this viewport a failure is returned.




## -see-also




<a href="https://msdn.microsoft.com/6EDFBA93-D2A2-4089-9976-CD1F8421B319">IDirectManipulationViewport2</a>
 

 

