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

# D2D1_DRAW_TEXT_OPTIONS enumeration


## -description


Specifies whether text snapping is suppressed or clipping to the layout rectangle is enabled. This enumeration allows a bitwise combination of its member values.


## -enum-fields




### -field D2D1_DRAW_TEXT_OPTIONS_NO_SNAP

Text is not vertically snapped to pixel boundaries. This setting is recommended for text that is being animated. 


### -field D2D1_DRAW_TEXT_OPTIONS_CLIP

Text is clipped to the layout rectangle.


### -field D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT

In Windows 8.1 and later, text is rendered using color versions of glyphs, if defined by the font.


### -field D2D1_DRAW_TEXT_OPTIONS_DISABLE_COLOR_BITMAP_SNAPPING

Bitmap origins of color glyph bitmaps are not snapped.


### -field D2D1_DRAW_TEXT_OPTIONS_NONE

Text is vertically snapped to pixel boundaries and is not clipped to the layout rectangle. 


### -field D2D1_DRAW_TEXT_OPTIONS_FORCE_DWORD




## -see-also




<a href="https://msdn.microsoft.com/1e3517cc-9c68-418e-b62e-a9ca06019efa">DrawText</a>
 

 

