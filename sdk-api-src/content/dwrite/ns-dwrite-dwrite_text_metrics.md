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

# DWRITE_TEXT_METRICS structure


## -description


Contains the metrics associated with text after layout. 
  All coordinates are in device independent pixels (DIPs).


## -struct-fields




### -field left

Type: <b>FLOAT</b>

A value that indicates the left-most point of formatted text relative to the layout box, 
	  while excluding any glyph overhang.


### -field top

Type: <b>FLOAT</b>

A value that indicates the top-most point of formatted text relative to the layout box, while excluding any glyph overhang.


### -field width

Type: <b>FLOAT</b>

A value that indicates the width of the formatted text, while ignoring trailing whitespace 
	  at the end of each line.


### -field widthIncludingTrailingWhitespace

Type: <b>FLOAT</b>

The width of the formatted text, taking into account the 
	  trailing whitespace at the end of each line.


### -field height

Type: <b>FLOAT</b>

The height of the formatted text. The height of an empty string 
	  is set to the same value as that of the default font.


### -field layoutWidth

Type: <b>FLOAT</b>

The initial width given to the layout. It can be either larger or smaller than the 
	  text content width, depending on whether the text 
	  was wrapped.


### -field layoutHeight

Type: <b>FLOAT</b>

Initial height given to the layout. Depending on the length of the text, it may be larger or smaller than the text content height.


### -field maxBidiReorderingDepth

Type: <b>UINT32</b>

The maximum reordering count of any line of text, used 
	  to calculate the most number of hit-testing boxes needed. 
	  If the layout has no bidirectional text, or no text at all, 
	  the minimum level is 1.


### -field lineCount

Type: <b>UINT32</b>

Total number of lines.

