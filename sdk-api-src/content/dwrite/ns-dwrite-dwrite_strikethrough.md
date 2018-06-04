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

# DWRITE_STRIKETHROUGH structure


## -description


Contains information regarding the size and placement of strikethroughs.
  All coordinates are in device independent pixels (DIPs).


## -struct-fields




### -field width

Type: <b>FLOAT</b>

A value that indicates the width of the strikethrough, measured parallel to the baseline.


### -field thickness

Type: <b>FLOAT</b>

A value that indicates the thickness of the strikethrough, measured perpendicular to the baseline.


### -field offset

Type: <b>FLOAT</b>

A value that indicates the offset of the strikethrough from the baseline. 
	  A positive offset represents a position below the baseline and 
	  a negative offset is above.  Typically, the offset will be negative.


### -field readingDirection

Type: <b><a href="https://msdn.microsoft.com/37288d34-d533-474c-b3c0-8c6361074a9b">DWRITE_READING_DIRECTION</a></b>

Reading direction of the text associated with the strikethrough. 
	  This value is used to interpret whether the width value runs horizontally 
	  or vertically.


### -field flowDirection

Type: <b><a href="https://msdn.microsoft.com/35a78bde-ba80-4328-8fb8-77ca73c1c04b">DWRITE_FLOW_DIRECTION</a></b>

Flow direction of the text associated with the strikethrough. 
	  This value is used to interpret whether the thickness value advances top to 
	  bottom, left to right, or right to left.


### -field localeName

Type: <b>const WCHAR*</b>

An array of characters containing the locale of the  text that is the strikethrough is being drawn over. 


### -field measuringMode

Type: <b><a href="https://msdn.microsoft.com/99e89754-8bc2-457d-bfdb-a3c9ccfe00c1">DWRITE_MEASURING_MODE</a></b>

The measuring mode can be useful to the renderer to determine how underlines are rendered, such as rounding the thickness to a whole pixel in GDI-compatible modes.

