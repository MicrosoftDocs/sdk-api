---
UID: NF:dwrite_3.IDWriteFontResource.CreateFontFace
title: IDWriteFontResource::CreateFontFace
description: Creates a font face instance with specific axis values.
helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","CreateFontFace method","IDWriteFontResource.CreateFontFace","IDWriteFontResource::CreateFontFace","CreateFontFace","CreateFontFace method [Direct Write]","CreateFontFace method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_createfontface","dwrite_3/IDWriteFontResource::CreateFontFace"]
tech.root: DirectWrite
ms.date: 09/13/2019
ms.keywords: IDWriteFontResource interface [Direct Write],CreateFontFace method, IDWriteFontResource.CreateFontFace, IDWriteFontResource::CreateFontFace, CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_createfontface, dwrite_3/IDWriteFontResource::CreateFontFace
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
 - IDWriteFontResource::CreateFontFace
 - dwrite_3/IDWriteFontResource::CreateFontFace
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
 - IDWriteFontResource::CreateFontFace
---

## -description

Creates a font face instance with specific axis values.

## -parameters

### -param fontSimulations

Type: **[DWRITE_FONT_SIMULATIONS](../dwrite/ne-dwrite-dwrite_font_simulations.md)**

Font face simulation flags for algorithmic emboldening and italicization.

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param fontFace [out]

Type: **[IDWriteFontFace5](./nn-dwrite_3-idwritefontface5.md)\*\***

The address of a pointer to an [IDWriteFontFace5](./nn-dwrite_3-idwritefontface5.md) interface. On successful completion, the function sets the pointer to a newly created font face object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DWRITE_E_REMOTEFONT|The font is not local.|

## -remarks

The axis values that you provide are permitted to be a subset or superset of all the ones actually supported by the font. Any unspecified axes use their default values: values beyond the ranges are clamped, and any non-varying axes have no effect.

## -see-also
