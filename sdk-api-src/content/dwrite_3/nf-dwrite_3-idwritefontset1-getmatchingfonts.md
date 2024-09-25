---
UID: NF:dwrite_3.IDWriteFontSet1.GetMatchingFonts
title: IDWriteFontSet1::GetMatchingFonts
description: Retrieves a matching font set based on the requested inputs, ordered so that nearer matches are earlier.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","GetMatchingFonts method","IDWriteFontSet1.GetMatchingFonts","IDWriteFontSet1::GetMatchingFonts","GetMatchingFonts","GetMatchingFonts method [Direct Write]","GetMatchingFonts method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_getmatchingfonts","dwrite_3/IDWriteFontSet1::GetMatchingFonts"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],GetMatchingFonts method, IDWriteFontSet1.GetMatchingFonts, IDWriteFontSet1::GetMatchingFonts, GetMatchingFonts, GetMatchingFonts method [Direct Write], GetMatchingFonts method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_getmatchingfonts, dwrite_3/IDWriteFontSet1::GetMatchingFonts
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
 - IDWriteFontSet1::GetMatchingFonts
 - dwrite_3/IDWriteFontSet1::GetMatchingFonts
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
 - IDWriteFontSet1::GetMatchingFonts
---

## -description

Retrieves a matching font set based on the requested inputs, ordered so that nearer matches are earlier.

## -parameters

### -param fontProperty

Type: **[DWRITE_FONT_PROPERTY](./ns-dwrite_3-dwrite_font_property.md) const \***

Font property of interest, such as typographic family or weight/stretch/style family.

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param matchingFonts

Type: **[IDWriteFontSet1](./nn-dwrite_3-idwritefontset1.md)\*\***

The address of a pointer to an [IDWriteFontSet1](./nn-dwrite_3-idwritefontset1.md) interface. On successful completion, the function sets the pointer to a prioritized list of fonts that match the properties, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

This method can yield distinct items that were not in the original font set, including items with simulation flags (if they would be a closer match to the request), and instances that were not named by the font author. Items from the same font resources are collapsed into one: the closest possible match.

## -see-also
