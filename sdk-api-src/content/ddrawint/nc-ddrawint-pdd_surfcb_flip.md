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

# PDD_SURFCB_FLIP callback function


## -description


The <b>DdFlip</b> callback function causes the surface memory associated with the target surface to become the primary surface, and the current surface to become the nonprimary surface.


## -parameters




### -param Arg1








#### - lpFlip

Points to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551520">DD_FLIPDATA</a> structure that contains the information required to perform the flip.


## -returns



<b>DdFlip</b> returns one of the following callback codes:




## -remarks



<b>DdFlip</b> allows a display driver to perform multibuffering. DirectDraw drivers must implement this function.

The driver should update its surface pointers so that the next frame will be written to the surface to which the <b>lpSurfTarg</b> member of the DD_FLIPDATA structure at <b>lpFlip</b> points. If a previous flip request is still pending, the driver should fail the call by setting the <b>ddRVal</b> member of DD_FLIPDATA to DDERR_WASSTILLDRAWING and returning DDHAL_DRIVER_HANDLED. The driver should ensure that the scan line is not in the vertical blank before performing the flip. <b>DdFlip</b> does not affect the actual display of the video data.

If the driver's hardware supports overlays or textures, <b>DdFlip</b> should make any necessary checks based on the surface type before performing the flip.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff551520">DD_FLIPDATA</a>
 

 

