---
UID: NF:gdiplusstringformat.StringFormat.GetDigitSubstitutionMethod
title: StringFormat::GetDigitSubstitutionMethod (gdiplusstringformat.h)
description: The StringFormat::GetDigitSubstitutionMethod method gets an element of the StringDigitSubstitute enumeration that indicates the digit substitution method that is used by this StringFormat object.
helpviewer_keywords: ["GetDigitSubstitutionMethod","GetDigitSubstitutionMethod method [GDI+]","GetDigitSubstitutionMethod method [GDI+]","StringFormat class","StringFormat class [GDI+]","GetDigitSubstitutionMethod method","StringFormat.GetDigitSubstitutionMethod","StringFormat::GetDigitSubstitutionMethod","_gdiplus_CLASS_StringFormat_GetDigitSubstitutionMethod_","gdiplus._gdiplus_CLASS_StringFormat_GetDigitSubstitutionMethod_"]
old-location: gdiplus\_gdiplus_CLASS_StringFormat_GetDigitSubstitutionMethod_.htm
tech.root: gdiplus
ms.assetid: VS|gdicpp|~\gdiplus\gdiplusreference\classes\stringformatclass\stringformatmethods\getdigitsubstitutionmethod.htm
ms.date: 12/05/2018
ms.keywords: GetDigitSubstitutionMethod, GetDigitSubstitutionMethod method [GDI+], GetDigitSubstitutionMethod method [GDI+],StringFormat class, StringFormat class [GDI+],GetDigitSubstitutionMethod method, StringFormat.GetDigitSubstitutionMethod, StringFormat::GetDigitSubstitutionMethod, _gdiplus_CLASS_StringFormat_GetDigitSubstitutionMethod_, gdiplus._gdiplus_CLASS_StringFormat_GetDigitSubstitutionMethod_
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
 - StringFormat::GetDigitSubstitutionMethod
 - gdiplusstringformat/StringFormat::GetDigitSubstitutionMethod
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
 - StringFormat.GetDigitSubstitutionMethod
---

# StringFormat::GetDigitSubstitutionMethod


## -description

The <b>StringFormat::GetDigitSubstitutionMethod</b> method gets an element of the 
			<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a> enumeration that indicates the digit substitution method that is used by this 
			<a href="/windows/desktop/api/gdiplusstringformat/nl-gdiplusstringformat-stringformat">StringFormat</a> object.



## -returns

Type: <b><a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a></b>

This method returns an element of the 
						<a href="/windows/desktop/api/gdiplusenums/ne-gdiplusenums-stringdigitsubstitute">StringDigitSubstitute</a> enumeration.

## -remarks

The digit substitution method replaces, in a string, Western European digits with digits that correspond to a user's locale or language.
