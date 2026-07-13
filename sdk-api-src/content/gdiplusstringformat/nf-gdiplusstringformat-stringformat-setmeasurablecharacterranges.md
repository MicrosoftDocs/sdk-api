---
UID: NF:gdiplusstringformat.StringFormat.SetMeasurableCharacterRanges
title: StringFormat::SetMeasurableCharacterRanges (gdiplusstringformat.h)
description: The StringFormat::SetMeasurableCharacterRanges method sets a series of character ranges for this StringFormat object that, when in a string, can be measured by the MeasureCharacterRanges method.
helpviewer_keywords: ["SetMeasurableCharacterRanges","SetMeasurableCharacterRanges method [GDI+]","SetMeasurableCharacterRanges method [GDI+]","StringFormat class","StringFormat class [GDI+]","SetMeasurableCharacterRanges method","StringFormat.SetMeasurableCharacterRanges","StringFormat::SetMeasurableCharacterRanges","_gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_","gdiplus._gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\setmeasurablecharacterranges.htm
ms.date: 12/05/2018
ms.keywords: SetMeasurableCharacterRanges, SetMeasurableCharacterRanges method [GDI+], SetMeasurableCharacterRanges method [GDI+],StringFormat class, StringFormat class [GDI+],SetMeasurableCharacterRanges method, StringFormat.SetMeasurableCharacterRanges, StringFormat::SetMeasurableCharacterRanges, _gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_, gdiplus._gdiplus_CLASS_StringFormat_SetMeasurableCharacterRanges_rangeCount_ranges_
req.header: gdiplusstringformat.h
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
 - StringFormat::SetMeasurableCharacterRanges
 - gdiplusstringformat/StringFormat::SetMeasurableCharacterRanges
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
 - StringFormat.SetMeasurableCharacterRanges
---

## -description

The <b>StringFormat::SetMeasurableCharacterRanges</b> method sets a series of character ranges for this <a href="/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object that, when in a string, can be measured by the <a href="/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-measurecharacterranges">MeasureCharacterRanges</a> method.

## -parameters

### -param rangeCount [in]

Type: <b>INT</b>

Integer that specifies the number of character ranges in the <i>ranges</i> array (no more than 32).

### -param ranges [in]

Type: <b>const <a href="/windows/win32/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a>*</b>

Pointer to an array of <a href="/windows/win32/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a> objects that specify the character ranges to be measured.

## -returns

Type: <b><a href="/windows/win32/api/gdiplustypes/ne-gdiplustypes-status">Status</a></b>

If the method succeeds, it returns Ok, which is an element of the <a href="/windows/win32/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

If the method fails, it returns one of the other elements of the <a href="/windows/win32/api/gdiplustypes/ne-gdiplustypes-status">Status</a> enumeration.

## -see-also

<a href="/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-measurecharacterranges">MeasureCharacterRanges</a>



<a href="/windows/win32/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a>



<a href="/windows/win32/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-getmeasurablecharacterrangecount">StringFormat::GetMeasurableCharacterRangeCount</a>
