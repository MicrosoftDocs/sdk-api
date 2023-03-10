---
UID: NF:gdiplusheaders.FontFamily.GetLineSpacing
title: FontFamily::GetLineSpacing (gdiplusheaders.h)
description: The FontFamily::GetLineSpacing method gets the line spacing, in design units, of this font family for the specified style or style combination. The line spacing is the vertical distance between the base lines of two consecutive lines of text.
helpviewer_keywords: ["FontFamily class [GDI+]","GetLineSpacing method","FontFamily.GetLineSpacing","FontFamily::GetLineSpacing","GetLineSpacing","GetLineSpacing method [GDI+]","GetLineSpacing method [GDI+]","FontFamily class","_gdiplus_CLASS_FontFamily_GetLineSpacing_style_","gdiplus._gdiplus_CLASS_FontFamily_GetLineSpacing_style_"]
old-location: gdiplus\_gdiplus_CLASS_FontFamily_GetLineSpacing_style_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\fontfamilyclass\fontfamilymethods\getlinespacing.htm
ms.date: 12/05/2018
ms.keywords: FontFamily class [GDI+],GetLineSpacing method, FontFamily.GetLineSpacing, FontFamily::GetLineSpacing, GetLineSpacing, GetLineSpacing method [GDI+], GetLineSpacing method [GDI+],FontFamily class, _gdiplus_CLASS_FontFamily_GetLineSpacing_style_, gdiplus._gdiplus_CLASS_FontFamily_GetLineSpacing_style_
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
 - FontFamily::GetLineSpacing
 - gdiplusheaders/FontFamily::GetLineSpacing
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
 - FontFamily.GetLineSpacing
---

# FontFamily::GetLineSpacing


## -description

The <b>FontFamily::GetLineSpacing</b> method gets the line spacing, in design units, of this font family for the specified style or style combination. The line spacing is the vertical distance between the base lines of two consecutive lines of text.

## -parameters

### -param style [in]

Type: <b>INT</b>

Integer that specifies the style of the typeface. This value must be an element of the <a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a> enumeration or the result of a bitwise <b>OR</b> applied to two or more of these elements. For example, <code>FontStyleBold | FontStyleUnderline | FontStyleStrikeout</code> specifies a combination of the three styles.

## -returns

Type: <b>UINT16</b>

This method returns the line spacing of this font family.

## -see-also

<a href="/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily">FontFamily</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontfamily-getcellascent">FontFamily::GetCellAscent</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontfamily-getcelldescent">FontFamily::GetCellDescent</a>



<a href="/windows/desktop/api/gdiplusheaders/nf-gdiplusheaders-fontfamily-getemheight">FontFamily::GetEmHeight</a>



<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-fontstyle">FontStyle</a>



<a href="/windows/desktop/gdiplus/-gdiplus-obtaining-font-metrics-use">Obtaining Font Metrics</a>