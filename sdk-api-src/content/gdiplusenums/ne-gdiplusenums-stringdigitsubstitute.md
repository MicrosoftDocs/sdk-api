---
UID: NE:gdiplusenums.StringDigitSubstitute
title: StringDigitSubstitute (gdiplusenums.h)
description: The StringDigitSubstitute enumeration specifies how to substitute digits in a string according to a user's locale or language.
helpviewer_keywords: ["StringDigitSubstitute","StringDigitSubstitute enumeration [GDI+]","StringDigitSubstituteNational","StringDigitSubstituteNone","StringDigitSubstituteTraditional","StringDigitSubstituteUser","_gdiplus_ENUM_StringDigitSubstitute","gdiplus._gdiplus_ENUM_StringDigitSubstitute","gdiplusenums/StringDigitSubstitute","gdiplusenums/StringDigitSubstituteNational","gdiplusenums/StringDigitSubstituteNone","gdiplusenums/StringDigitSubstituteTraditional","gdiplusenums/StringDigitSubstituteUser"]
old-location: gdiplus\_gdiplus_ENUM_StringDigitSubstitute.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\enumerations\stringdigitsubstitute.htm
ms.date: 12/05/2018
ms.keywords: StringDigitSubstitute, StringDigitSubstitute enumeration [GDI+], StringDigitSubstituteNational, StringDigitSubstituteNone, StringDigitSubstituteTraditional, StringDigitSubstituteUser, _gdiplus_ENUM_StringDigitSubstitute, gdiplus._gdiplus_ENUM_StringDigitSubstitute, gdiplusenums/StringDigitSubstitute, gdiplusenums/StringDigitSubstituteNational, gdiplusenums/StringDigitSubstituteNone, gdiplusenums/StringDigitSubstituteTraditional, gdiplusenums/StringDigitSubstituteUser
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
targetos: Windows
req.typenames: 
req.redist: 
req.product: GDI+ 1.0
ms.custom: 19H1
f1_keywords:
 - StringDigitSubstitute
 - gdiplusenums/StringDigitSubstitute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Gdiplusenums.h
api_name:
 - StringDigitSubstitute
---

# StringDigitSubstitute enumeration


## -description

The <b>StringDigitSubstitute</b> enumeration specifies how to substitute digits in a string according to a user's locale or language.

## -enum-fields

### -field StringDigitSubstituteUser:0

Specifies a user-defined substitution scheme.

### -field StringDigitSubstituteNone:1

Specifies to disable substitutions.

### -field StringDigitSubstituteNational:2

Specifies substitution digits that correspond with the official national language of the user's locale.

### -field StringDigitSubstituteTraditional:3

Specifies substitution digits that correspond with the user's native script or language, which may be different from the official national language of the user's locale.

