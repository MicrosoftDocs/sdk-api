---
UID: NF:gdiplusheaders.Bitmap.InitializePalette
title: Bitmap::InitializePalette
author: windows-sdk-content
description: The Bitmap::InitializePalette method initializes a standard, optimal, or custom color palette.
old-location: gdiplus\_gdiplus_CLASS_Bitmap_InitializePalette_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\bitmapclass\bitmapgethistogrammethods\initializepalette.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Bitmap class [GDI+],InitializePalette method, Bitmap.InitializePalette, Bitmap::InitializePalette, InitializePalette, InitializePalette method [GDI+], InitializePalette method [GDI+],Bitmap class, _gdiplus_CLASS_Bitmap_InitializePalette_, gdiplus._gdiplus_CLASS_Bitmap_InitializePalette_
ms.topic: method
req.header: gdiplusheaders.h
req.include-header: Gdiplus.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Bitmap.InitializePalette
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.1
---

# Bitmap::InitializePalette


## -description


The <b>Bitmap::InitializePalette</b> method initializes a standard, optimal, or custom color palette.


## -parameters




### -param palette [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a>*</b>

Pointer to a buffer that contains a <a href="https://msdn.microsoft.com/en-us/library/ms534064(v=VS.85).aspx">ColorPalette</a> structure followed by an array of <b>ARGB</b> values. The <b>Entries</b> member of a <b>ColorPalette</b> structure is an array of one <b>ARGB</b> value. You must allocate memory for the <b>ColorPalette</b> structure and for the additional <b>ARGB</b> values in the palette. For example, if the palette has 36 <b>ARGB</b> values, allocate a buffer as follows: <code>malloc(sizeof(ColorPalette) + 35*sizeof(ARGB))</code>.


### -param palettetype [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534159(v=VS.85).aspx">PaletteType</a></b>

Element of the <a href="https://msdn.microsoft.com/en-us/library/ms534159(v=VS.85).aspx">PaletteType</a> enumeration that specifies the palette type. The palette can have one of several standard types, or it can be a custom palette that you define. Also, the <b>Bitmap::InitializePalette</b> method can create an optimal palette based on a specified bitmap.


### -param optimalColors [in]

Type: <b>INT</b>

Integer that specifies the number of colors you want to have in an optimal palette based on a specified bitmap. If this parameter is greater than 0, the <i>palettetype</i> parameter must be set to <b>PaletteTypeOptimal</b>, and the <i>bitmap</i> parameter must point to a <a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object. If you are creating a standard or custom palette rather than an optimal palette, set this parameter to 0.


### -param useTransparentColor [in]

Type: <b>BOOL</b>

Boolean value that specifies whether to include the transparent color in the palette. Set to <b>TRUE</b> to include the transparent color; otherwise <b>FALSE</b>.


### -param bitmap [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>*</b>

Pointer to a <a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a> object for which an optimal palette will be created. If <i>palettetype</i> is set to <b>PaletteTypeOptimal</b> and <i>optimalColors</i> is set to a positive integer, set this parameter to the address of a <b>Bitmap</b> object. Otherwise, set this parameter to <b>NULL</b>.


## -returns



Type: <strong>Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a></b>
</strong>

If the method succeeds, it returns <b>Ok</b>, which is an element of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.

If the method fails, it returns one of the other elements of the 
						<a href="https://msdn.microsoft.com/en-us/library/ms534175(v=VS.85).aspx">Status</a> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms534420(v=VS.85).aspx">Bitmap</a>
 

 

