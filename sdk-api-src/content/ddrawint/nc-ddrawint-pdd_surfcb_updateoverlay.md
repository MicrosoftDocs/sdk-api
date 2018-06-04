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

# PDD_SURFCB_UPDATEOVERLAY callback function


## -description


The <b>DdUpdateOverlay</b> callback function repositions or modifies the visual attributes of an overlay surface.


## -parameters




### -param Arg1








#### - lpUpdateOverlay

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551751">DD_UPDATEOVERLAYDATA</a> structure that contains the information required to update the overlay.


## -returns



<b>DdUpdateOverlay</b> returns one of the following callback codes:




## -remarks



<b>DdUpdateOverlay</b> shows, hides, or repositions an overlay surface on the screen. It also sets attributes of the overlay surface, such as the stretch factor or type of color key to be used.

The driver should determine whether it has the bandwidth to support the overlay update request. The driver should use the <b>dwFlags</b> member of the DD_UPDATEOVERLAYDATA structure at <b>lpUpdateOverlay</b> to determine the type of request and how to process it.

The driver/hardware must stretch or shrink the overlay accordingly when the rectangles specified by the <b>rDest</b> and <b>rSrc</b> members of DD_UPDATEOVERLAYDATA are different sizes.

Note that <a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a> is used for flipping between overlay surfaces, so performance for <b>DdUpdateOverlay</b> is not critical.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551751">DD_UPDATEOVERLAYDATA</a>



<a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a>



<a href="https://msdn.microsoft.com/4b4ee889-15c8-4a7c-a9d8-adab27b271dd">DdSetColorKey</a>



<a href="https://msdn.microsoft.com/0bafdeea-d06d-4c25-9ee5-b7df23d7dd20">DdSetOverlayPosition</a>
 

 

