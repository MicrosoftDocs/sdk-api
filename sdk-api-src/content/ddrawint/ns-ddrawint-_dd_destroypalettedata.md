---
UID: NS:ddrawint._DD_DESTROYPALETTEDATA
title: "_DD_DESTROYPALETTEDATA"
author: windows-sdk-content
description: The DD_DESTROYPALETTEDATA structure contains information necessary to destroy the specified palette.
old-location: display\dd_destroypalettedata.htm
tech.root: display
ms.assetid: e309f782-bd0b-4703-b58c-e202fd87b904
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PDD_DESTROYPALETTEDATA, DD_DESTROYPALETTEDATA, DD_DESTROYPALETTEDATA structure [Display Devices], _DD_DESTROYPALETTEDATA, ddrawint/DD_DESTROYPALETTEDATA, ddstrcts_850bb816-b0df-4877-8903-c85b15074e30.xml, display.dd_destroypalettedata"
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
 - DD_DESTROYPALETTEDATA
product: Windows
targetos: Windows
req.typenames: "*PDD_DESTROYPALETTEDATA, DD_DESTROYPALETTEDATA"
req.redist: 
---

# _DD_DESTROYPALETTEDATA structure


## -description


The DD_DESTROYPALETTEDATA structure contains information necessary to destroy the specified palette.


## -struct-fields




### -field lpDD

Points to the <a href="https://msdn.microsoft.com/a59f064b-48cf-4491-82cd-84f59467af87">DD_DIRECTDRAW_GLOBAL</a> structure that describes the driver's device.


### -field lpDDPalette

Points to the <a href="https://msdn.microsoft.com/3ec5b950-c0b4-4a50-bdac-fb53c757f1f1">DD_PALETTE_GLOBAL</a> structure representing the palette object to be destroyed. 


### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/b44936fd-0052-4f54-9e97-1664c381c697">DdDestroyPalette</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


### -field DestroyPalette

Used by the Microsoft DirectDraw API and should not be filled in by the driver.


## -see-also




<a href="https://msdn.microsoft.com/b44936fd-0052-4f54-9e97-1664c381c697">DdDestroyPalette</a>
 

 

