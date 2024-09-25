---
UID: NF:dwrite_3.IDWriteFontSet1.CreateFontFace
title: IDWriteFontSet1::CreateFontFace
description: Creates a font face for a single item (rather than going through the font face reference).
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","CreateFontFace method","IDWriteFontSet1.CreateFontFace","IDWriteFontSet1::CreateFontFace","CreateFontFace","CreateFontFace method [Direct Write]","CreateFontFace method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_createfontface","dwrite_3/IDWriteFontSet1::CreateFontFace"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],CreateFontFace method, IDWriteFontSet1.CreateFontFace, IDWriteFontSet1::CreateFontFace, CreateFontFace, CreateFontFace method [Direct Write], CreateFontFace method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_createfontface, dwrite_3/IDWriteFontSet1::CreateFontFace
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
 - IDWriteFontSet1::CreateFontFace
 - dwrite_3/IDWriteFontSet1::CreateFontFace
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
 - IDWriteFontSet1::CreateFontFace
---

## -description

Creates a font face for a single item (rather than going through the font face reference).

## -parameters

### -param listIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Zero-based index of the font item in the set.

### -param fontFace [out]

Type: **[IDWriteFontFace5](./nn-dwrite_3-idwritefontface5.md)\*\***

The address of a pointer to an [IDWriteFontFace5](./nn-dwrite_3-idwritefontface5.md) interface. On successful completion, the function sets the pointer to a newly created font face object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|DWRITE_E_REMOTEFONT|The font is not local.|

## -remarks

## -see-also
