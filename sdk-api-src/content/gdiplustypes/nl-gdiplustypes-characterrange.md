---
UID: NL:gdiplustypes.CharacterRange
title: CharacterRange (gdiplustypes.h)
description: A CharacterRange object specifies a range of character positions within a string.
helpviewer_keywords: ["CharacterRange","CharacterRange class [GDI+]","CharacterRange class [GDI+]","described","_gdiplus_CLASS_CharacterRange_Class","gdiplus._gdiplus_CLASS_CharacterRange_Class","gdiplustypes/CharacterRange"]
old-location: gdiplus\_gdiplus_CLASS_CharacterRange_Class.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\characterrange.htm
ms.date: 12/05/2018
ms.keywords: CharacterRange, CharacterRange class [GDI+], CharacterRange class [GDI+],described, _gdiplus_CLASS_CharacterRange_Class, gdiplus._gdiplus_CLASS_CharacterRange_Class, gdiplustypes/CharacterRange
req.header: gdiplustypes.h
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
 - CharacterRange
 - gdiplustypes/CharacterRange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - gdiplustypes.h
api_name:
 - CharacterRange
---

# CharacterRange class


## -description

A <a href="/previous-versions/ms536266(v=vs.85)">CharacterRange</a> object specifies a range of character positions within a string.


## -remarks

A character range is a range of character positions within a string of text. The area of the display that is occupied by a group of characters that are specified by the character range is the bounding region. A character range is set by 
				<b>StringFormat::SetMeasurableCharacterRanges</b>. The number of ranges that are currently set can be determined by calling 
				<b>StringFormat::GetMeasurableCharacterRangeCount</b>. This number is also the number of regions expected to be obtained by the 
				<b>MeasureCharacterRanges</b> method.
