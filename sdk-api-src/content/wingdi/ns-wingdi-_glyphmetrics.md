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

# _GLYPHMETRICS structure


## -description



The <b>GLYPHMETRICS</b> structure contains information about the placement and orientation of a glyph in a character cell.




## -struct-fields




### -field gmBlackBoxX

The width of the smallest rectangle that completely encloses the glyph (its black box).


### -field gmBlackBoxY

The height of the smallest rectangle that completely encloses the glyph (its black box).


### -field gmptGlyphOrigin

The x- and y-coordinates of the upper left corner of the smallest rectangle that completely encloses the glyph.


### -field gmCellIncX

The horizontal distance from the origin of the current character cell to the origin of the next character cell.


### -field gmCellIncY

The vertical distance from the origin of the current character cell to the origin of the next character cell.


## -remarks



Values in the <b>GLYPHMETRICS</b> structure are specified in device units.




## -see-also




<a href="https://msdn.microsoft.com/93726d5c-d4ed-4681-bf45-cb899f195b5d">Font and Text Structures</a>



<a href="https://msdn.microsoft.com/9944baa9-8e50-40b9-9650-78b0b1d7643a">Fonts and Text Overview</a>



<a href="https://msdn.microsoft.com/08f06007-5b21-44ab-b234-21a58c94ed4e">GetGlyphOutline</a>
 

 

