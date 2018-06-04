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

# WICBitmapPaletteType enumeration


## -description


Specifies the type of palette used for an indexed image format.


## -enum-fields




### -field WICBitmapPaletteTypeCustom

An arbitrary custom palette provided by caller.


### -field WICBitmapPaletteTypeMedianCut

An optimal palette generated using a median-cut algorithm. Derived from the colors in an image.


### -field WICBitmapPaletteTypeFixedBW

A black and white palette.


### -field WICBitmapPaletteTypeFixedHalftone8

A palette that has its 8-color on-off primaries and the 16 system colors added. With duplicates removed, 16 colors are available.


### -field WICBitmapPaletteTypeFixedHalftone27

A palette that has 3 intensity levels of each primary: 27-color on-off primaries and the 16 system colors added. With duplicates removed, 35 colors are available.


### -field WICBitmapPaletteTypeFixedHalftone64

A palette that has 4 intensity levels of each primary: 64-color on-off primaries and the 16 system colors added. With duplicates removed, 72 colors are available.


### -field WICBitmapPaletteTypeFixedHalftone125

A palette that has 5 intensity levels of each primary: 125-color on-off primaries and the 16 system colors added. With duplicates removed, 133 colors are available.


### -field WICBitmapPaletteTypeFixedHalftone216

A palette that has 6 intensity levels of each primary: 216-color on-off primaries and the 16 system colors added. With duplicates removed, 224 colors are available. This is the same as <b>WICBitmapPaletteFixedHalftoneWeb</b>.


### -field WICBitmapPaletteTypeFixedWebPalette

A palette that has 6 intensity levels of each primary: 216-color on-off primaries and the 16 system colors added. With duplicates removed, 224 colors are available. This is the same as <b>WICBitmapPaletteTypeFixedHalftone216</b>.


### -field WICBitmapPaletteTypeFixedHalftone252

A palette that has its 252-color on-off primaries and the 16 system colors added. With duplicates removed, 256 colors are available.


### -field WICBitmapPaletteTypeFixedHalftone256

A palette that has its 256-color on-off primaries and the 16 system colors added. With duplicates removed, 256 colors are available.


### -field WICBitmapPaletteTypeFixedGray4

A palette that has 4 shades of gray.


### -field WICBitmapPaletteTypeFixedGray16

A palette that has 16 shades of gray.


### -field WICBitmapPaletteTypeFixedGray256

A palette that has 256 shades of gray.


### -field WICBITMAPPALETTETYPE_FORCE_DWORD



