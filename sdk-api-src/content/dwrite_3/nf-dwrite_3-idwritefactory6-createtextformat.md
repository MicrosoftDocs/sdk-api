---
UID: NF:dwrite_3.IDWriteFactory6.CreateTextFormat
title: IDWriteFactory6::CreateTextFormat
description: Creates a text format object used for text layout.I
helpviewer_keywords: ["IDWriteFactory6 interface [Direct Write]","CreateTextFormat method","IDWriteFactory6.CreateTextFormat","IDWriteFactory6::CreateTextFormat","CreateTextFormat","CreateTextFormat method [Direct Write]","CreateTextFormat method [Direct Write]","IDWriteFactory6 interface","directwrite.idwritefactory6_createtextformat","dwrite_3/IDWriteFactory6::CreateTextFormat"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteFactory6 interface [Direct Write],CreateTextFormat method, IDWriteFactory6.CreateTextFormat, IDWriteFactory6::CreateTextFormat, CreateTextFormat, CreateTextFormat method [Direct Write], CreateTextFormat method [Direct Write],IDWriteFactory6 interface, directwrite.idwritefactory6_createtextformat, dwrite_3/IDWriteFactory6::CreateTextFormat
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
 - IDWriteFactory6::CreateTextFormat
 - dwrite_3/IDWriteFactory6::CreateTextFormat
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
 - IDWriteFactory6::CreateFontSetBuilder
---

## -description

Creates a text format object used for text layout.

## -parameters

### -param fontFamilyName

Type: **[WCHAR](/windows/win32/winprog/windows-data-types) const \***

Name of the font family from the collection.

### -param fontCollection

Type: **[IDWriteFontCollection](../dwrite/nn-dwrite-idwritefontcollection.md)\***

Font collection. Use `nullptr` to indicate the system font collection.

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param fontSize

Type: **[FLOAT](/windows/win32/winprog/windows-data-types)**

Logical size of the font in DIP units.

### -param localeName

Type: **[WCHAR](/windows/win32/winprog/windows-data-types) const \***

Locale name (for example, "ja-JP", "en-US", "ar-EG").

### -param textFormat

Type: **[IDWriteTextFormat3](./nn-dwrite_3-idwritetextformat3.md)\*\***

The address of a pointer to an [IDWriteTextFormat3](./nn-dwrite_3-idwritetextformat3.md) interface. On successful completion, the function sets the pointer to a newly created text format object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

If *fontCollection* is `nullptr`, then the system font collection is used, grouped by typographic family name ([DWRITE_FONT_FAMILY_MODEL_TYPOGRAPHIC](./ne-dwrite_3-dwrite_font_family_model.md)) without downloadable fonts.

## -see-also
