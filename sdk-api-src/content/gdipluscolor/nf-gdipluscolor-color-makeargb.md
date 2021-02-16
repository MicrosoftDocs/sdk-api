---
UID: NF:gdipluscolor.Color.MakeARGB
title: Color::MakeARGB (gdipluscolor.h)
description: The Color::MakeARGB method creates a 32-bit value that consolidates the specified alpha, red, green, and blue components.
helpviewer_keywords: ["Color class [GDI+]","MakeARGB method","Color.MakeARGB","Color::MakeARGB","MakeARGB","MakeARGB method [GDI+]","MakeARGB method [GDI+]","Color class","_gdiplus_CLASS_Color_MakeARGB_a_r_g_b_","gdiplus._gdiplus_CLASS_Color_MakeARGB_a_r_g_b_"]
old-location: gdiplus\_gdiplus_CLASS_Color_MakeARGB_a_r_g_b_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorclass\colormethods\makeargb.htm
ms.date: 12/05/2018
ms.keywords: Color class [GDI+],MakeARGB method, Color.MakeARGB, Color::MakeARGB, MakeARGB, MakeARGB method [GDI+], MakeARGB method [GDI+],Color class, _gdiplus_CLASS_Color_MakeARGB_a_r_g_b_, gdiplus._gdiplus_CLASS_Color_MakeARGB_a_r_g_b_
req.header: gdipluscolor.h
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
req.lib: Gdiplus.lib
req.dll: Gdiplus.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - Color::MakeARGB
 - gdipluscolor/Color::MakeARGB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gdiplus.dll
api_name:
 - Color.MakeARGB
---

# Color::MakeARGB


## -description

The <b>Color::MakeARGB</b> method creates a 32-bit value that consolidates the specified alpha, red, green, and blue components.

## -parameters

### -param a [in]

Type: <b>BYTE</b>

Byte that specifies the alpha component.

### -param r [in]

Type: <b>BYTE</b>

Byte that specifies the red component.

### -param g [in]

Type: <b>BYTE</b>

Byte that specifies the green component.

### -param b [in]

Type: <b>BYTE</b>

Byte that specifies the blue component.

## -returns

Type: <b>static</b>

This method returns an <b>ARGB</b> value that holds the specified alpha, red, green, and blue components.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-getvalue">Color::GetValue</a>



<a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-setfromcolorref">Color::SetFromCOLORREF</a>