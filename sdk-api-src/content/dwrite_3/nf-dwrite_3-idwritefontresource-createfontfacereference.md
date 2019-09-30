---
UID: NF:dwrite_3.IDWriteFontResource.CreateFontFaceReference
title: IDWriteFontResource::CreateFontFaceReference
author: windows-sdk-content
description: Creates a font face reference with specific axis values.
tech.root: DirectWrite
ms.author: windowssdkdev
ms.date: 09/10/2019
ms.keywords: IDWriteFontResource interface [Direct Write],CreateFontFaceReference method, IDWriteFontResource.CreateFontFaceReference, IDWriteFontResource::CreateFontFaceReference, CreateFontFaceReference, CreateFontFaceReference method [Direct Write], CreateFontFaceReference method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_createfontfacereference, dwrite_3/IDWriteFontResource::CreateFontFaceReference
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFontResource.CreateFontFaceReference"
req.construct-type: function
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Dwrite.lib
 - Dwrite.dll
api_name:
 - IDWriteFontResource::CreateFontFaceReference
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Creates a font face reference with specific axis values.

## -parameters

### -param fontSimulations

Type: **[DWRITE_FONT_SIMULATIONS](/windows/win32/api/dwrite/ne-dwrite-dwrite_font_simulations)**

Font face simulation flags for algorithmic emboldening and italicization.

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param fontFaceReference [out]

Type: **[IDWriteFontFaceReference1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1)\*\***

The address of a pointer to an [IDWriteFontFaceReference1](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) interface. On successful completion, the function sets the pointer to a newly created font face reference object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

The axis values that you provide are permitted to be a subset or superset of all the ones actually supported by the font. Any unspecified axes use their default values: values beyond the ranges are clamped, and any non-varying axes have no effect.

## -see-also