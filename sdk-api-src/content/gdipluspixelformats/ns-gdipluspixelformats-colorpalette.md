---
UID: NS:gdipluspixelformats.ColorPalette
title: ColorPalette
author: windows-sdk-content
description: The ColorPalette structure defines an array of colors that make up a color palette. The colors are 32-bit ARGB colors.
old-location: gdiplus\_gdiplus_STRUC_ColorPalette.htm
old-project: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\structures\colorpalette.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: ColorPalette, ColorPalette structure [GDI+], _gdiplus_STRUC_ColorPalette, gdiplus._gdiplus_STRUC_ColorPalette, gdipluspixelformats/ColorPalette
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdipluspixelformats.h
api_name:
 - ColorPalette
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

Combination of flags from the <a href="https://msdn.microsoft.com/en-us/library/ms534158(v=VS.85).aspx">PaletteFlags</a> enumeration. 


### -field Count

Type: <b>UINT</b>

Number of elements in the <b>Entries</b> array.


### -field Entries

Type: <b>ARGB[1]</b>

Array of ARGB colors. 


## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/mt297756">Color</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535384(v=VS.85).aspx">Image::GetPalette</a>



<a href="https://msdn.microsoft.com/en-us/library/ms535404(v=VS.85).aspx">Image::SetPalette</a>



<a href="https://msdn.microsoft.com/en-us/library/ms536393(v=VS.85).aspx">Types of Bitmaps</a>
 

 

