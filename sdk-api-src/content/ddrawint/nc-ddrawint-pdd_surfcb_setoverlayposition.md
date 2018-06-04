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

# PDD_SURFCB_SETOVERLAYPOSITION callback function


## -description


The <b>DdSetOverlayPosition</b> callback function sets the position for an overlay.


## -parameters




### -param Arg1








#### - lpSetOverlayPosition

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551706">DD_SETOVERLAYPOSITIONDATA</a> structure that contains the information required to set the overlay position.


## -returns



<b>DdSetOverlayPosition</b> returns one of the following callback codes:




## -remarks



When the overlay is visible, the driver should cause the overlay to be displayed on the primary surface. The upper left corner of the overlay should be anchored at the position specified by the <b>lXPos</b> and <b>lYPos</b> members of the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551706">DD_SETOVERLAYPOSITIONDATA</a> structure at <i>lpSetOverlayPosition</i>. For example, values of (0,0) indicate that the upper left corner of the overlay should appear in the upper left corner of the surface identified by the <b>lpDDDestSurface</b> member of DD_SETOVERLAYPOSITIONDATA.

When the overlay is invisible, the driver should set an error code in the <b>ddRVal</b> member of DD_SETOVERLAYPOSITIONDATA and return DDHAL_DRIVER_HANDLED.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551706">DD_SETOVERLAYPOSITIONDATA</a>
 

 

