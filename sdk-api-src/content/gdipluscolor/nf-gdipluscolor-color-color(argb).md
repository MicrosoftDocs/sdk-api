---
UID: NF:gdipluscolor.Color.Color(ARGB)
title: Color::Color(IN ARGB) (gdipluscolor.h)
description: Creates a Color::Color object by using an ARGB value.
helpviewer_keywords: ["Color","Color class [GDI+]","Color constructor","Color constructor [GDI+]","Color constructor [GDI+]","Color class","Color.Color","Color.Color(ARGB)","Color.Color(IN ARGB)","Color::Color","Color::Color(IN ARGB)","_gdiplus_CLASS_Color_Color_argb_","gdiplus._gdiplus_CLASS_Color_Color_argb_"]
old-location: gdiplus\_gdiplus_CLASS_Color_Color_argb_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\colorclass\colorconstructors\color_63argb.htm
ms.date: 12/05/2018
ms.keywords: Color, Color class [GDI+],Color constructor, Color constructor [GDI+], Color constructor [GDI+],Color class, Color.Color, Color.Color(ARGB), Color.Color(IN ARGB), Color::Color, Color::Color(IN ARGB), _gdiplus_CLASS_Color_Color_argb_, gdiplus._gdiplus_CLASS_Color_Color_argb_
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
 - Color::Color
 - gdipluscolor/Color::Color
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
 - Color.Color
---

# Color::Color(IN ARGB)


## -description

Creates a <b>Color::Color</b> object by using an 
			<b>ARGB</b> value.

## -parameters

### -param argb [in]

Type: <b>ARGB</b>

Value that specifies the alpha, red, green, and blue color components.

## -remarks

An 
				<b>ARGB</b> value is a <b>DWORD</b> that contains the alpha, red, green, and blue components of a color. 
				<b>ARGB</b> is defined in Gdipluspixelformats.h.

## -see-also

<a href="/windows/desktop/api/gdipluscolor/nl-gdipluscolor-color">Color</a>



<a href="/previous-versions/ms536243(v=vs.85)">Color Constructors</a>



<a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-makeargb">Color::MakeARGB</a>