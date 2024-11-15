---
UID: NF:dwrite_3.IDWriteFontFamily2.GetMatchingFonts
title: IDWriteFontFamily2::GetMatchingFonts
description: Retrieves a list of fonts in the font family, ranked in order of how well they match the specified axis values.
helpviewer_keywords: ["IDWriteFontFamily2 interface [Direct Write]","GetMatchingFonts method","IDWriteFontFamily2.GetMatchingFonts","IDWriteFontFamily2::GetMatchingFonts","GetMatchingFonts","GetMatchingFonts method [Direct Write]","GetMatchingFonts method [Direct Write]","IDWriteFontFamily2 interface","directwrite.idwritefontfamily2_getmatchingfont","dwrite_3/IDWriteFontFamily2::GetMatchingFonts"]
tech.root: DirectWrite
ms.date: 09/12/2019
ms.keywords: IDWriteFontFamily2 interface [Direct Write],GetMatchingFonts method, IDWriteFontFamily2.GetMatchingFonts, IDWriteFontFamily2::GetMatchingFonts, GetMatchingFonts, GetMatchingFonts method [Direct Write], GetMatchingFonts method [Direct Write],IDWriteFontFamily2 interface, directwrite.idwritefontfamily2_getmatchingfont, dwrite_3/IDWriteFontFamily2::GetMatchingFonts
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
 - IDWriteFontFamily2::GetMatchingFonts
 - dwrite_3/IDWriteFontFamily2::GetMatchingFonts
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
 - IDWriteFontFamily2::GetMatchingFonts
---

## -description

Retrieves a list of fonts in the font family, ranked in order of how well they match the specified axis values.

## -parameters

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param matchingFonts [out]

Type: **[IDWriteFontList2](./nn-dwrite_3-idwritefontlist2.md)\*\***

The address of a pointer to an [IDWriteFontList2](./nn-dwrite_3-idwritefontlist2.md) interface. On successful completion, the function sets the pointer to a newly created font list object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
