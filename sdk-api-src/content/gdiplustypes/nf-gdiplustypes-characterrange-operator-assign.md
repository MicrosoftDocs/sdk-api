---
UID: NF:gdiplustypes.CharacterRange.operator-assign
title: CharacterRange::operator-assign (gdiplustypes.h)
description: The CharacterRange::operator= method sets this CharacterRange object equal to the specified CharacterRange object.
helpviewer_keywords: ["CharacterRange class [GDI+]","operator= method","CharacterRange.operator-assign","CharacterRange.operator=","CharacterRange::operator-assign","CharacterRange::operator=","_gdiplus_CLASS_CharacterRange_operator_rhs_","gdiplus._gdiplus_CLASS_CharacterRange_operator_rhs_","operator=","operator= method [GDI+]","operator= method [GDI+]","CharacterRange class"]
old-location: gdiplus\_gdiplus_CLASS_CharacterRange_operator_rhs_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\characterrangeclass\operator.htm
ms.date: 12/05/2018
ms.keywords: CharacterRange class [GDI+],operator= method, CharacterRange.operator-assign, CharacterRange.operator=, CharacterRange::operator-assign, CharacterRange::operator=, _gdiplus_CLASS_CharacterRange_operator_rhs_, gdiplus._gdiplus_CLASS_CharacterRange_operator_rhs_, operator=, operator= method [GDI+], operator= method [GDI+],CharacterRange class
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
 - CharacterRange::operator=
 - gdiplustypes/CharacterRange::operator=
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
 - CharacterRange.operator=
---

# CharacterRange::operator-assign


## -description

The <b>CharacterRange::operator=</b> method sets this <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a> object equal to the specified <b>CharacterRange</b> object.

## -parameters

### -param rhs [in, ref]

Type: <b>const <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a></b>

Reference to a <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a> object that is assigned to this <b>CharacterRange</b> object.

## -returns

Type: <b><a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a></b>

This method returns a reference to this <a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a> object to allow cascaded assignments.

## -see-also

<a href="/windows/desktop/api/gdiplustypes/nl-gdiplustypes-characterrange">CharacterRange</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-getmeasurablecharacterrangecount">GetMeasurableCharacterRangeCount</a>



<a href="/windows/desktop/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-measurecharacterranges">MeasureCharacterRanges</a>



<a href="/windows/desktop/api/gdiplusstringformat/nf-gdiplusstringformat-stringformat-setmeasurablecharacterranges">SetMeasurableCharacterRanges</a>