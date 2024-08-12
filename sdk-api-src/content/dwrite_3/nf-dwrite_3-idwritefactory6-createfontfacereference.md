---
UID: NF:dwrite_3.IDWriteFactory6.CreateFontFaceReference
title: IDWriteFactory6::CreateFontFaceReference
description: Creates a reference to a specific font instance within a file.
helpviewer_keywords: ["IDWriteFactory6 interface [Direct Write]","CreateFontFaceReference method","IDWriteFactory6.CreateFontFaceReference","IDWriteFactory6::CreateFontFaceReference","CreateFontFaceReference","CreateFontFaceReference method [Direct Write]","CreateFontFaceReference method [Direct Write]","IDWriteFactory6 interface","directwrite.idwritefactory6_createfontfacereference","dwrite_3/IDWriteFactory6::CreateFontFaceReference"]
tech.root: DirectWrite
ms.date: 09/10/2019
ms.keywords: IDWriteFactory6 interface [Direct Write],CreateFontFaceReference method, IDWriteFactory6.CreateFontFaceReference, IDWriteFactory6::CreateFontFaceReference, CreateFontFaceReference, CreateFontFaceReference method [Direct Write], CreateFontFaceReference method [Direct Write],IDWriteFactory6 interface, directwrite.idwritefactory6_createfontfacereference, dwrite_3/IDWriteFactory6::CreateFontFaceReference
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
 - IDWriteFactory6::CreateFontFaceReference
 - dwrite_3/IDWriteFactory6::CreateFontFaceReference
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
 - IDWriteFactory6::CreateFontFaceReference
---

## -description

Creates a reference to a specific font instance within a file.

## -parameters

### -param fontFile

Type: **[IDWriteFontFile](../dwrite/nn-dwrite-idwritefontfile.md)\***

A user-provided font file representing the font face.

### -param faceIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The zero-based index of a font face in cases when the font file contains a collection of font faces. If the font file contains a single face, then set this value to zero.

### -param fontSimulations

Type: **[DWRITE_FONT_SIMULATIONS](../dwrite/ne-dwrite-dwrite_font_simulations.md)**

Font face simulation flags for algorithmic emboldening and italicization.

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

### -param fontFaceReference [out]

Type: **[IDWriteFontFaceReference1](./nn-dwrite_3-idwritefontfacereference1.md)\*\***

The address of a pointer to an [IDWriteFontFaceReference1](./nn-dwrite_3-idwritefontfacereference1.md) interface. On successful completion, the function sets the pointer to a newly created font face reference object, otherwise it sets the pointer to `nullptr`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
