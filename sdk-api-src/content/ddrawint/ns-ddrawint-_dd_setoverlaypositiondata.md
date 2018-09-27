---
UID: NS:ddrawint._DD_SETOVERLAYPOSITIONDATA
title: "_DD_SETOVERLAYPOSITIONDATA"
author: windows-sdk-content
description: The DD_SETOVERLAYPOSITIONDATA structure contains information necessary to change the display coordinates of an overlay surface.
old-location: display\dd_setoverlaypositiondata.htm
tech.root: display
ms.assetid: edfcbe23-81af-41fb-b29e-cd6e2da4d603
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*PDD_SETOVERLAYPOSITIONDATA, DD_SETOVERLAYPOSITIONDATA, DD_SETOVERLAYPOSITIONDATA structure [Display Devices], _DD_SETOVERLAYPOSITIONDATA, ddrawint/DD_SETOVERLAYPOSITIONDATA, ddstrcts_963680b2-05c1-4f15-959c-c38a8141541b.xml, display.dd_setoverlaypositiondata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: ddrawint.h
req.include-header: Winddi.h
req.target-type: Windows
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
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_SETOVERLAYPOSITIONDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_SETOVERLAYPOSITIONDATA, DD_SETOVERLAYPOSITIONDATA"
req.redist: 
---

# _DD_SETOVERLAYPOSITIONDATA structure


## -description


The DD_SETOVERLAYPOSITIONDATA structure contains information necessary to change the display coordinates of an overlay surface.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSrcSurface

Points to a <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure that represents the Microsoft DirectDraw overlay surface.


### -field lpDDDestSurface

Points to a DD_SURFACE_LOCAL structure representing the surface that is being overlaid.


### -field lXPos

Specifies the x-coordinate of the upper left corner of the overlay, in pixels.


### -field lYPos

Specifies the y coordinate of the upper left corner of the overlay, in pixels.


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/0bafdeea-d06d-4c25-9ee5-b7df23d7dd20">DdSetOverlayPosition</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field SetOverlayPosition

Used by the DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/0bafdeea-d06d-4c25-9ee5-b7df23d7dd20">DdSetOverlayPosition</a>
 

 

