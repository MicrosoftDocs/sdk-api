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

# IDirectManipulationViewport2::AddBehavior


## -description


Adds a behavior to the viewport and returns a cookie to the caller.


## -parameters




### -param behavior [in]

A behavior created using the <a href="https://msdn.microsoft.com/8890E44F-595A-4116-B4A4-F10FAEE598B7">CreateBehavior</a> method.


### -param cookie [out, retval]

A cookie is returned so the caller can remove this behavior later. This allows the caller to release any reference on the behavior and let <a href="https://msdn.microsoft.com/26358bc5-71e9-40f0-9243-9bddd961a0e5">Direct Manipulation</a> maintain an appropriate lifetime, similar to event handlers. 


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. Attaching a behavior that is already attached to this viewport or another viewport results in a failure.




## -remarks



A behavior takes effect immediately after <b>AddBehavior</b> is called. This must be considered when adding a behavior during an active manipulation or inertia phase.




## -see-also




<a href="https://msdn.microsoft.com/6EDFBA93-D2A2-4089-9976-CD1F8421B319">IDirectManipulationViewport2</a>
 

 

