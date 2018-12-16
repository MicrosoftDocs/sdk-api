---
UID: NE:d2d1.D2D1_DRAW_TEXT_OPTIONS
title: D2D1_DRAW_TEXT_OPTIONS
author: windows-sdk-content
description: Specifies whether text snapping is suppressed or clipping to the layout rectangle is enabled. This enumeration allows a bitwise combination of its member values.
old-location: direct2d\D2D1_DRAW_TEXT_OPTIONS.htm
tech.root: direct2d
ms.assetid: 30f5be4a-83c2-4039-8e09-00e842fc5eb2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: D2D1_DRAW_TEXT_OPTIONS, D2D1_DRAW_TEXT_OPTIONS enumeration [Direct2D], D2D1_DRAW_TEXT_OPTIONS_CLIP, D2D1_DRAW_TEXT_OPTIONS_DISABLE_COLOR_BITMAP_SNAPPING, D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT, D2D1_DRAW_TEXT_OPTIONS_NONE, D2D1_DRAW_TEXT_OPTIONS_NO_SNAP, d2d1/D2D1_DRAW_TEXT_OPTIONS, d2d1/D2D1_DRAW_TEXT_OPTIONS_CLIP, d2d1/D2D1_DRAW_TEXT_OPTIONS_DISABLE_COLOR_BITMAP_SNAPPING, d2d1/D2D1_DRAW_TEXT_OPTIONS_ENABLE_COLOR_FONT, d2d1/D2D1_DRAW_TEXT_OPTIONS_NONE, d2d1/D2D1_DRAW_TEXT_OPTIONS_NO_SNAP, direct2d.D2D1_DRAW_TEXT_OPTIONS
ms.topic: enum
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - d2d1.h
api_name:
 - D2D1_DRAW_TEXT_OPTIONS
product: Windows
targetos: Windows
req.typenames: D2D1_DRAW_TEXT_OPTIONS
req.redist: 
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
 

 

