---
UID: NF:dwrite_3.IDWriteFontSetBuilder2.AddFont
title: IDWriteFontSetBuilder2::AddFont
description: Adds a font to the set being built.
helpviewer_keywords: ["IDWriteFontSetBuilder2 interface [Direct Write]","AddFont method","IDWriteFontSetBuilder2.AddFont","IDWriteFontSetBuilder2::AddFont","AddFont","AddFont method [Direct Write]","AddFont method [Direct Write]","IDWriteFontSetBuilder2 interface","directwrite.idwritefontsetbuilder2_addfont","dwrite_3/IDWriteFontSetBuilder2::AddFont"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSetBuilder2 interface [Direct Write],AddFont method, IDWriteFontSetBuilder2.AddFont, IDWriteFontSetBuilder2::AddFont, AddFont, AddFont method [Direct Write], AddFont method [Direct Write],IDWriteFontSetBuilder2 interface, directwrite.idwritefontsetbuilder2_addfont, dwrite_3/IDWriteFontSetBuilder2::AddFont
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
 - IDWriteFontSetBuilder2::AddFont
 - dwrite_3/IDWriteFontSetBuilder2::AddFont
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
 - IDWriteFontSetBuilder2::AddFont
---

## -description

Adds a font to the set being built, with the caller supplying enough information to search on and determine axis ranges, avoiding the need to open the potentially non-local font.

## -parameters

### -param fontFile

Type: **[IDWriteFontFile](../dwrite/nn-dwrite-idwritefontfile.md)\***

Font file reference object to add to the set.

### -param fontFaceIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The zero-based index of a font face in a collection.

### -param fontSimulations

Type: **[DWRITE_FONT_SIMULATIONS](../dwrite/ne-dwrite-dwrite_font_simulations.md)**

Font face simulation flags for algorithmic emboldening and italicization.

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param fontAxisRanges

Type: **[DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md) const \***

List of axis ranges.

### -param fontAxisRangeCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Number of axis ranges.

### -param properties

Type: **[DWRITE_FONT_PROPERTY](./ns-dwrite_3-dwrite_font_property.md) const \***

List of properties to associate with the reference.

### -param propertyCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of properties defined.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

The font properties should include at least a family (typographic or weight/style/stretch). Otherwise the font would be accessible in the **IDWriteFontSet** only by index, not name.

## -see-also
