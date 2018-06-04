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

# DWRITE_GLYPH_IMAGE_DATA structure


## -description


Data for a single glyph from GetGlyphImageData.


## -struct-fields




### -field imageData

Pointer to the glyph data.


### -field imageDataSize

Size of glyph data in bytes.


### -field uniqueDataId

Unique identifier for the glyph data. Clients may use this to cache a parsed/decompressed version and tell whether a repeated call to the same font returns the same data.


### -field pixelsPerEm

Pixels per em of the returned data. For non-scalable raster data (PNG/TIFF/JPG), this can be larger or smaller than requested from GetGlyphImageData when there isn't an exact match.
          For scaling intermediate sizes, use: desired pixels per em * font em size / actual pixels per em.


### -field pixelSize

Size of image when the format is pixel data.


### -field horizontalLeftOrigin

Left origin along the horizontal Roman baseline.


### -field horizontalRightOrigin

Right origin along the horizontal Roman baseline.


### -field verticalTopOrigin

Top origin along the vertical central baseline.


### -field verticalBottomOrigin

Bottom origin along vertical central baseline.

