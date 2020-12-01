---
UID: NF:gdiplustypes.CharacterRange.CharacterRange(INT,INT)
title: CharacterRange::CharacterRange(INT,INT) (gdiplustypes.h)
description: Creates a CharacterRange::CharacterRange object and initializes the data members to the values specified.
helpviewer_keywords: ["CharacterRange","CharacterRange class [GDI+]","CharacterRange constructor","CharacterRange constructor [GDI+]","CharacterRange constructor [GDI+]","CharacterRange class","CharacterRange.CharacterRange","CharacterRange.CharacterRange(INT","INT)","CharacterRange::CharacterRange","CharacterRange::CharacterRange(INT","INT)","_gdiplus_CLASS_CharacterRange_CharacterRange_first_length_","gdiplus._gdiplus_CLASS_CharacterRange_CharacterRange_first_length_"]
old-location: gdiplus\_gdiplus_CLASS_CharacterRange_CharacterRange_first_length_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\characterrangeclass\characterrangeconstructors\characterrange_68first_length.htm
ms.date: 12/05/2018
ms.keywords: CharacterRange, CharacterRange class [GDI+],CharacterRange constructor, CharacterRange constructor [GDI+], CharacterRange constructor [GDI+],CharacterRange class, CharacterRange.CharacterRange, CharacterRange.CharacterRange(INT,INT), CharacterRange::CharacterRange, CharacterRange::CharacterRange(INT,INT), _gdiplus_CLASS_CharacterRange_CharacterRange_first_length_, gdiplus._gdiplus_CLASS_CharacterRange_CharacterRange_first_length_
req.header: gdiplustypes.h
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
 - CharacterRange::CharacterRange
 - gdiplustypes/CharacterRange::CharacterRange
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
 - CharacterRange.CharacterRange
---

# CharacterRange::CharacterRange(INT,INT)


## -description

Creates a <b>CharacterRange::CharacterRange</b> object and initializes the data members to the values specified.

## -parameters

### -param first [in]

Type: <b>INT</b>

Integer that specifies the first position of this range. For example, if 
					<i>first</i> is set to 0, then the first position of this range is position 0 in the string.

### -param length [in]

Type: <b>INT</b>

Integer that specifies the number of positions in this range.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-getmeasurablecharacterrangecount">GetMeasurableCharacterRangeCount</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-measurecharacterranges">MeasureCharacterRanges</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-setmeasurablecharacterranges">SetMeasurableCharacterRanges</a>