---
UID: NC:ddrawint.PDD_SURFCB_UPDATEOVERLAY
title: PDD_SURFCB_UPDATEOVERLAY
author: windows-sdk-content
description: The DdUpdateOverlay callback function repositions or modifies the visual attributes of an overlay surface.
old-location: display\ddupdateoverlay.htm
tech.root: display
ms.assetid: e86b3b75-319a-4817-bcb1-59580c855ef9
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: DdUpdateOverlay, DdUpdateOverlay callback function [Display Devices], PDD_SURFCB_UPDATEOVERLAY, PDD_SURFCB_UPDATEOVERLAY callback, ddfncs_aa6e3770-06c5-4be1-b934-2eb58f909f30.xml, ddrawint/DdUpdateOverlay, display.ddupdateoverlay
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Desktop
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - ddrawint.h
api_name:
 - DdUpdateOverlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDD_SURFCB_UPDATEOVERLAY callback function


## -description


The <b>DdUpdateOverlay</b> callback function repositions or modifies the visual attributes of an overlay surface.


## -parameters




### -param Arg1








#### - lpUpdateOverlay

Points to a <a href="https://msdn.microsoft.com/f9dd3fe3-1295-40c8-83d9-74861945921e">DD_UPDATEOVERLAYDATA</a> structure that contains the information required to update the overlay.


## -returns



<b>DdUpdateOverlay</b> returns one of the following callback codes:




## -remarks



<b>DdUpdateOverlay</b> shows, hides, or repositions an overlay surface on the screen. It also sets attributes of the overlay surface, such as the stretch factor or type of color key to be used.

The driver should determine whether it has the bandwidth to support the overlay update request. The driver should use the <b>dwFlags</b> member of the DD_UPDATEOVERLAYDATA structure at <b>lpUpdateOverlay</b> to determine the type of request and how to process it.

The driver/hardware must stretch or shrink the overlay accordingly when the rectangles specified by the <b>rDest</b> and <b>rSrc</b> members of DD_UPDATEOVERLAYDATA are different sizes.

Note that <a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a> is used for flipping between overlay surfaces, so performance for <b>DdUpdateOverlay</b> is not critical.




## -see-also




<a href="https://msdn.microsoft.com/f9dd3fe3-1295-40c8-83d9-74861945921e">DD_UPDATEOVERLAYDATA</a>



<a href="https://msdn.microsoft.com/4ce2e967-7b4a-4065-844d-d8852dec8a8f">DdFlip</a>



<a href="https://msdn.microsoft.com/4b4ee889-15c8-4a7c-a9d8-adab27b271dd">DdSetColorKey</a>



<a href="https://msdn.microsoft.com/0bafdeea-d06d-4c25-9ee5-b7df23d7dd20">DdSetOverlayPosition</a>
 

 

