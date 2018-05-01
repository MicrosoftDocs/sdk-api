---
UID: NS:gdipluspixelformats.ColorPalette
title: ColorPalette
author: windows-driver-content
description: The ColorPalette structure defines an array of colors that make up a color palette. The colors are 32-bit ARGB colors.
old-location: gdiplus\_gdiplus_STRUC_ColorPalette.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorpalette.htm
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: ColorPalette, ColorPalette structure [GDI+], _gdiplus_STRUC_ColorPalette, gdiplus._gdiplus_STRUC_ColorPalette, gdipluspixelformats/ColorPalette
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: gdipluspixelformats.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Gdipluspixelformats.h
api_name:
-	ColorPalette
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.0
---

# ColorPalette structure


## -description


The <b>ColorPalette</b> structure defines an array of colors that make up a color palette. The colors are 32-bit ARGB colors.


## -struct-fields




### -field Flags

Type: <b>UINT</b>

Combination of flags from the <a href="https://msdn.microsoft.com/60b44f93-600a-4041-bcee-ac75fa9339c9">PaletteFlags</a> enumeration. 


### -field Count

Type: <b>UINT</b>

Number of elements in the <b>Entries</b> array.


### -field Entries

Type: <b>ARGB[1]</b>

Array of ARGB colors. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/ffe250ce-0ebc-4470-846f-f45a1de5165e">Image::GetPalette</a>



<a href="https://msdn.microsoft.com/62f1c8c0-788b-41e6-91af-15019b65bc3d">Image::SetPalette</a>



<a href="https://msdn.microsoft.com/fac60d01-d07e-41e9-98a3-34c592d97a92">Types of Bitmaps</a>
 

 

