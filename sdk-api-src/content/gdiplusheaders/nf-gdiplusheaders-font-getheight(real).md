---
UID: NF:gdiplusheaders.Font.GetHeight(REAL)
title: Font::GetHeight(IN REAL) (gdiplusheaders.h)
description: The Font::GetHeight method gets the line spacing, in pixels, of this font.
helpviewer_keywords: ["Font class [GDI+]","GetHeight method","Font.GetHeight","Font.GetHeight(IN REAL)","Font.GetHeight(REAL)","Font::GetHeight","Font::GetHeight(IN REAL)","GetHeight","GetHeight method [GDI+]","GetHeight method [GDI+]","Font class","_gdiplus_CLASS_Font_GetHeight_dpi_","gdiplus._gdiplus_CLASS_Font_GetHeight_dpi_"]
old-location: gdiplus\_gdiplus_CLASS_Font_GetHeight_dpi_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontclass\fontmethods\fontgetheightmethods\getheight_84dpi.htm
ms.date: 12/05/2018
ms.keywords: Font class [GDI+],GetHeight method, Font.GetHeight, Font.GetHeight(IN REAL), Font.GetHeight(REAL), Font::GetHeight, Font::GetHeight(IN REAL), GetHeight, GetHeight method [GDI+], GetHeight method [GDI+],Font class, _gdiplus_CLASS_Font_GetHeight_dpi_, gdiplus._gdiplus_CLASS_Font_GetHeight_dpi_
req.header: gdiplusheaders.h
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
 - Font::GetHeight
 - gdiplusheaders/Font::GetHeight
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
 - Font.GetHeight
---

# Font::GetHeight(IN REAL)


## -description

The <b>Font::GetHeight</b> method gets the line spacing, in pixels, of this font. The line spacing is the vertical distance between the base lines of two consecutive lines of text. Thus, the line spacing includes the blank space between lines along with the height of the character itself.

## -parameters

### -param dpi [in]

Type: <b>REAL</b>

Real number that specifies the vertical resolution, in dots per inch, of the device that displays the font.

## -returns

Type: <b>REAL</b>

This method returns the line spacing of the font in pixels.

## -remarks

If the font unit is set to anything other than <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-unit">UnitPixel</a>, the height, in pixels, is calculated using the specified vertical resolution. For example, suppose the font unit is inches and the font size is 0.3. Also suppose that for the corresponding font family, the em height is 2048 and the line spacing is 2355. If the specified vertical resolution is 96 dots per inch, the height is calculated as follows:

2355*(0.3/2048)*96 = 33.1171875

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font">Font</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-getsize">Font::GetSize</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-getstyle">Font::GetStyle</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-font-getunit">Font::GetUnit</a>



<a href="/windows/desktop/gdiplus/-gdiplus-using-text-and-fonts-use">Using Text and Fonts</a>