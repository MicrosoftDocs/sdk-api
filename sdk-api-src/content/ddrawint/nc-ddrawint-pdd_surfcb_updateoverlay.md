---
UID: NC:ddrawint.PDD_SURFCB_UPDATEOVERLAY
title: PDD_SURFCB_UPDATEOVERLAY (ddrawint.h)
description: The DdUpdateOverlay callback function repositions or modifies the visual attributes of an overlay surface.helpviewer_keywords: ["DdUpdateOverlay","DdUpdateOverlay callback function [Display Devices]","PDD_SURFCB_UPDATEOVERLAY","PDD_SURFCB_UPDATEOVERLAY callback","ddfncs_aa6e3770-06c5-4be1-b934-2eb58f909f30.xml","ddrawint/DdUpdateOverlay","display.ddupdateoverlay"]
old-location: display\ddupdateoverlay.htm
tech.root: display
ms.assetid: e86b3b75-319a-4817-bcb1-59580c855ef9
ms.date: 12/05/2018
ms.keywords: DdUpdateOverlay, DdUpdateOverlay callback function [Display Devices], PDD_SURFCB_UPDATEOVERLAY, PDD_SURFCB_UPDATEOVERLAY callback, ddfncs_aa6e3770-06c5-4be1-b934-2eb58f909f30.xml, ddrawint/DdUpdateOverlay, display.ddupdateoverlay
f1_keywords:
- ddrawint/DdUpdateOverlay
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PDD_SURFCB_UPDATEOVERLAY callback function


## -description


The <b>DdUpdateOverlay</b> callback function repositions or modifies the visual attributes of an overlay surface.


## -parameters




### -param Arg1








#### - lpUpdateOverlay

Points to a <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_updateoverlaydata">DD_UPDATEOVERLAYDATA</a> structure that contains the information required to update the overlay.


## -returns



<b>DdUpdateOverlay</b> returns one of the following callback codes:




## -remarks



<b>DdUpdateOverlay</b> shows, hides, or repositions an overlay surface on the screen. It also sets attributes of the overlay surface, such as the stretch factor or type of color key to be used.

The driver should determine whether it has the bandwidth to support the overlay update request. The driver should use the <b>dwFlags</b> member of the DD_UPDATEOVERLAYDATA structure at <b>lpUpdateOverlay</b> to determine the type of request and how to process it.

The driver/hardware must stretch or shrink the overlay accordingly when the rectangles specified by the <b>rDest</b> and <b>rSrc</b> members of DD_UPDATEOVERLAYDATA are different sizes.

Note that <a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a> is used for flipping between overlay surfaces, so performance for <b>DdUpdateOverlay</b> is not critical.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/ns-ddrawint-dd_updateoverlaydata">DD_UPDATEOVERLAYDATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_flip">DdFlip</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setcolorkey">DdSetColorKey</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ddrawint/nc-ddrawint-pdd_surfcb_setoverlayposition">DdSetOverlayPosition</a>
 

 

