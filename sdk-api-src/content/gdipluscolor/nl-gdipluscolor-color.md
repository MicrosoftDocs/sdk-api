---
UID: NL:gdipluscolor.Color
title: Color (gdipluscolor.h)
description: A Color object stores a 32-bit value that represents a color.
helpviewer_keywords: ["Color","Color class [GDI+]","Color class [GDI+]","described","_gdiplus_CLASS_Color_Class","gdiplus._gdiplus_CLASS_Color_Class","gdipluscolor/Color"]
old-location: gdiplus\_gdiplus_CLASS_Color_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\color.htm
ms.date: 12/05/2018
ms.keywords: Color, Color class [GDI+], Color class [GDI+],described, _gdiplus_CLASS_Color_Class, gdiplus._gdiplus_CLASS_Color_Class, gdipluscolor/Color
req.header: gdipluscolor.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Color
 - gdipluscolor/Color
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdipluscolor.h
api_name:
 - Color
---

# Color class


## -description

A <a href="/previous-versions/ms536243(v=vs.85)">Color</a> object stores a 32-bit value that represents a color. The color value contains four, 8-bit components: alpha, red, green, and blue. The first 8 bits (the most significant) contain the alpha component, the next 8 bits contain the red component, the next 8 bits contain the green component, and the next 8 bits (the least significant) contain the blue component. The 32-bit value is stored in a variable of type 
			<b>ARGB</b>.


## -remarks

The alpha component, the most significant 8 bits, specifies the transparency of a color. All four component values range from 0 to 255. An alpha component value of 0 specifies that the color is transparent, and an alpha value of 255 specifies that the color is opaque. Alpha component values from 1 through 254 specify the degree to which the color is blended with the background when the color is rendered. The red, green, and blue color component values range from 0 to 255 and determine the intensity of the color. The <a href="/windows/desktop/api/gdipluscolor/nf-gdipluscolor-color-makeargb">Color::MakeARGB</a> method is used to encapsulate the four color components into a single 32-bit value.
