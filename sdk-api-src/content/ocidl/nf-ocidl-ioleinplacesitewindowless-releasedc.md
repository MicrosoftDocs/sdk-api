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

# IOleInPlaceSiteWindowless::ReleaseDC


## -description


Releases the device context previously obtained by a call to <a href="https://msdn.microsoft.com/232587a8-ed88-4339-9e28-6e34be263a51">IOleInPlaceSiteWindowless::GetDC</a>.


## -parameters




### -param hDC [in]

The device context to be released.


## -returns



This method returns S_OK on success.




## -remarks



An object calls this method to notify its container that the object is done with the device context. If the device context was used for drawing, the container should ensure that all overlapping objects are repainted correctly. If the device context was an offscreen device context, its content should also be copied to the screen in the rectangle originally passed to <a href="https://msdn.microsoft.com/232587a8-ed88-4339-9e28-6e34be263a51">IOleInPlaceSiteWindowless::GetDC</a>. See <b>IOleInPlaceSiteWindowless::GetDC</b> for implementation notes relevant to <b>IOleInPlaceSiteWindowless::ReleaseDC</b>.




## -see-also




<a href="https://msdn.microsoft.com/4ad83599-99d2-4b35-95de-cff845a8d5e4">IOleInPlaceSiteWindowless</a>



<a href="https://msdn.microsoft.com/232587a8-ed88-4339-9e28-6e34be263a51">IOleInPlaceSiteWindowless::GetDC</a>
 

 

