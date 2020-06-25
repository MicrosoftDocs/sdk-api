---
UID: NE:gdiplusenums.StringTrimming
title: StringTrimming (gdiplusenums.h)
description: The StringTrimming enumeration specifies how to trim characters from a string so that the string fits into a layout rectangle. The layout rectangle is used to position and size the display string.
helpviewer_keywords: ["StringTrimming","StringTrimming enumeration [GDI+]","StringTrimmingCharacter","StringTrimmingEllipsisCharacter","StringTrimmingEllipsisPath","StringTrimmingEllipsisWord","StringTrimmingNone","StringTrimmingWord","_gdiplus_ENUM_StringTrimming","gdiplus._gdiplus_ENUM_StringTrimming","gdiplusenums/StringTrimming","gdiplusenums/StringTrimmingCharacter","gdiplusenums/StringTrimmingEllipsisCharacter","gdiplusenums/StringTrimmingEllipsisPath","gdiplusenums/StringTrimmingEllipsisWord","gdiplusenums/StringTrimmingNone","gdiplusenums/StringTrimmingWord"]
old-location: gdiplus\_gdiplus_ENUM_StringTrimming.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\stringtrimming.htm
ms.date: 12/05/2018
ms.keywords: StringTrimming, StringTrimming enumeration [GDI+], StringTrimmingCharacter, StringTrimmingEllipsisCharacter, StringTrimmingEllipsisPath, StringTrimmingEllipsisWord, StringTrimmingNone, StringTrimmingWord, _gdiplus_ENUM_StringTrimming, gdiplus._gdiplus_ENUM_StringTrimming, gdiplusenums/StringTrimming, gdiplusenums/StringTrimmingCharacter, gdiplusenums/StringTrimmingEllipsisCharacter, gdiplusenums/StringTrimmingEllipsisPath, gdiplusenums/StringTrimmingEllipsisWord, gdiplusenums/StringTrimmingNone, gdiplusenums/StringTrimmingWord
f1_keywords:
- gdiplusenums/StringTrimming
dev_langs:
- c++
req.header: gdiplusenums.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- Gdiplusenums.h
api_name:
- StringTrimming
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
---

# StringTrimming enumeration


## -description


The <b>StringTrimming</b> enumeration specifies how to trim characters from a string so that the string fits into a layout rectangle. The layout rectangle is used to position and size the display string.


## -enum-fields




### -field StringTrimmingNone

Specifies that no trimming is done. 


### -field StringTrimmingCharacter

Specifies that the string is broken at the boundary of the last character that is inside the layout rectangle. This is the default. 


### -field StringTrimmingWord

Specifies that the string is broken at the boundary of the last word that is inside the layout rectangle. 


### -field StringTrimmingEllipsisCharacter

Specifies that the string is broken at the boundary of the last character that is inside the layout rectangle and an ellipsis (...) is inserted after the character. 


### -field StringTrimmingEllipsisWord

Specifies that the string is broken at the boundary of the last word that is inside the layout rectangle and an ellipsis (...) is inserted after the word. 


### -field StringTrimmingEllipsisPath

Specifies that the center is removed from the string and replaced by an ellipsis. The algorithm keeps as much of the last portion of the string as possible. 


## -remarks



Trimming affects only the last visible or partly visible (due to clipping) line of text.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawstring(constwchar_int_constfont_constpointf__constbrush)">DrawString Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/gdiplus/-gdiplus-formatting-text-use">Formatting Text</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-measurestring(inconstwchar_inint_inconstfont_inconstpointf__inconststringformat_outrectf)">MeasureString Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringalignment">StringAlignment</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-settrimming">StringFormat::SetTrimming</a>



<a href="https://docs.microsoft.com/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringformatflags">StringFormatFlags</a>
 

 

