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

# WICPngFilterOption enumeration


## -description


Specifies the Portable Network Graphics (PNG) filters available for compression optimization.


## -enum-fields




### -field WICPngFilterUnspecified

Indicates an unspecified PNG filter. This enables WIC to algorithmically choose the best filtering option for the image.


### -field WICPngFilterNone

Indicates no PNG filter.


### -field WICPngFilterSub

Indicates a PNG sub filter.


### -field WICPngFilterUp

Indicates a PNG up filter.


### -field WICPngFilterAverage

Indicates a PNG average filter.


### -field WICPngFilterPaeth

Indicates a PNG paeth filter.


### -field WICPngFilterAdaptive

Indicates a PNG adaptive filter. This enables WIC to choose the best filtering mode on a per-scanline basis.


### -field WICPNGFILTEROPTION_FORCE_DWORD



