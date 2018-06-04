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

# D2D1_SVG_PAINT_TYPE enumeration


## -description


Specifies the paint type for an SVG fill or stroke.


## -enum-fields




### -field D2D1_SVG_PAINT_TYPE_NONE

The fill or stroke is not rendered.


### -field D2D1_SVG_PAINT_TYPE_COLOR

A solid color is rendered.


### -field D2D1_SVG_PAINT_TYPE_CURRENT_COLOR

The current color is rendered.


### -field D2D1_SVG_PAINT_TYPE_URI

A paint server, defined by another element in the SVG document, is used.


### -field D2D1_SVG_PAINT_TYPE_URI_NONE

A paint server, defined by another element in the SVG document, is used. If the paint server reference is invalid, fall back to D2D1_SVG_PAINT_TYPE_NONE.


### -field D2D1_SVG_PAINT_TYPE_URI_COLOR

A paint server, defined by another element in the SVG document, is used. If the paint server reference is invalid, fall back to D2D1_SVG_PAINT_TYPE_COLOR.


### -field D2D1_SVG_PAINT_TYPE_URI_CURRENT_COLOR

A paint server, defined by another element in the SVG document, is used. If the paint server reference is invalid, fall back to D2D1_SVG_PAINT_TYPE_CURRENT_COLOR.


### -field D2D1_SVG_PAINT_TYPE_FORCE_DWORD

