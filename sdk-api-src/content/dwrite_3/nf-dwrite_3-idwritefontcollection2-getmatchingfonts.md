---
UID: NF:dwrite_3.IDWriteFontCollection2.GetMatchingFonts
title: IDWriteFontCollection2::GetMatchingFonts
description: Retrieves a list of fonts in the specified font family, ranked in order of how well they match the specified axis values.
helpviewer_keywords: ["IDWriteFontCollection2 interface [Direct Write]","GetMatchingFonts method","IDWriteFontCollection2.GetMatchingFonts","IDWriteFontCollection2::GetMatchingFonts","GetMatchingFonts","GetMatchingFonts method [Direct Write]","GetMatchingFonts method [Direct Write]","IDWriteFontCollection2 interface","directwrite.idwritefontcollection2_getmatchingfont","dwrite_3/IDWriteFontCollection2::GetMatchingFonts"]
tech.root: DirectWrite
ms.date: 09/12/2019
ms.keywords: IDWriteFontCollection2 interface [Direct Write],GetMatchingFonts method, IDWriteFontCollection2.GetMatchingFonts, IDWriteFontCollection2::GetMatchingFonts, GetMatchingFonts, GetMatchingFonts method [Direct Write], GetMatchingFonts method [Direct Write],IDWriteFontCollection2 interface, directwrite.idwritefontcollection2_getmatchingfont, dwrite_3/IDWriteFontCollection2::GetMatchingFonts
req.construct-type: function
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 Build 16299
req.target-min-winversvr: Windows 10 Build 16299
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dwrite.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - IDWriteFontCollection2::GetMatchingFonts
 - dwrite_3/IDWriteFontCollection2::GetMatchingFonts
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontCollection2::GetMatchingFonts
---

## -description

Retrieves a list of fonts in the specified font family, ranked in order of how well they match the specified axis values.

## -parameters

### -param familyName

Type: **[WCHAR](/windows/win32/winprog/windows-data-types) const \***

Name of the font family. The name is not case-sensitive, but must otherwise exactly match a family name in the collection.

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param fontList [out]

Type: **[IDWriteFontList2](./nn-dwrite_3-idwritefontlist2.md)\*\***

The address of a pointer to an [IDWriteFontList2](./nn-dwrite_3-idwritefontlist2.md) interface. On successful completion, the function sets the pointer to a newly created font list object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

If no fonts match, an empty list object is returned (calling [IDWriteFontList::GetFontCount](../dwrite/nf-dwrite-idwritefontlist-getfontcount.md) on it returns 0), but the function doesn't return an error.

## -see-also
