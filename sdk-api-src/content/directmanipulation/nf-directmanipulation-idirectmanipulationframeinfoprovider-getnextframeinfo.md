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

# IDirectManipulationFrameInfoProvider::GetNextFrameInfo


## -description


Retrieves the composition timing information from the compositor.


## -parameters




### -param time [out]

The current time, in milliseconds.


### -param processTime [out]

The time, in milliseconds, when the compositor begins constructing the next frame.


### -param compositionTime [out]

The time, in milliseconds, when the compositor finishes composing and drawing the next frame on the screen.


## -returns



If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.




## -remarks



The system implementation of <a href="https://msdn.microsoft.com/15B7CA2A-DEC3-479B-BD41-38A57037002F">IDirectManipulationFrameInfoProvider</a> uses <a href="https://msdn.microsoft.com/40e2d02b-77e8-425f-ac5e-3dcddef08173">DirectComposition</a>. <a href="https://msdn.microsoft.com/C4DB7A16-BF91-4CD0-BCD2-4793D9599E0A">GetFrameStatistics</a> is used to calculate the parameter values for <b>GetNextFrameInfo</b>.




## -see-also




<a href="https://msdn.microsoft.com/b96b5e8f-fc11-48ad-83ca-96e23fd3ffc1">IDirectManipulationCompositor</a>



<a href="https://msdn.microsoft.com/15B7CA2A-DEC3-479B-BD41-38A57037002F">IDirectManipulationFrameInfoProvider</a>
 

 

