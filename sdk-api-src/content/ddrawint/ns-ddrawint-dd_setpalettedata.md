---
UID: NS:ddrawint._DD_SETPALETTEDATA
title: DD_SETPALETTEDATA (ddrawint.h)
author: windows-sdk-content
description: The DD_SETPALETTEDATA structure contains information necessary to set a palette for a specific surface.
old-location: display\dd_setpalettedata.htm
tech.root: display
ms.assetid: 943af430-19b2-481a-9cac-cd4cb767d96a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDD_SETPALETTEDATA, DD_SETPALETTEDATA, DD_SETPALETTEDATA structure [Display Devices], ddrawint/DD_SETPALETTEDATA, ddstrcts_254301f1-b163-4402-92b2-70a2632f5ebc.xml, display.dd_setpalettedata"
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
 - DD_SETPALETTEDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_SETPALETTEDATA, DD_SETPALETTEDATA"
req.redist: 
---

# DD_SETPALETTEDATA structure


## -description


The DD_SETPALETTEDATA structure contains information necessary to set a palette for a specific surface.


## -struct-fields




### -field lpDD

Points to a <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDSurface

Points to a <a href="https://msdn.microsoft.com/45a41cec-0257-4e26-809d-c2fc4c247328">DD_SURFACE_LOCAL</a> structure that represents the DirectDrawSurface object. 


### -field lpDDPalette

Points to a <a href="https://msdn.microsoft.com/3ec5b950-c0b4-4a50-bdac-fb53c757f1f1">DD_PALETTE_GLOBAL</a> structure that specifies the palette to set to the surface. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/745b30f0-3d2f-4894-8991-6b7d511f8493">DdSetPalette</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field SetPalette

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


### -field Attach

Indicates whether to attach this palette to the surface. 


## -see-also




<a href="https://msdn.microsoft.com/745b30f0-3d2f-4894-8991-6b7d511f8493">DdSetPalette</a>
 

 

