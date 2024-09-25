---
UID: NF:dwrite_3.IDWriteFontCollection2.GetFontFamily
title: IDWriteFontCollection2::GetFontFamily
description: Creates a font family object, given a zero-based font family index.
helpviewer_keywords: ["IDWriteFontCollection2 interface [Direct Write]","GetFontFamily method","IDWriteFontCollection2.GetFontFamily","IDWriteFontCollection2::GetFontFamily","GetFontFamily","GetFontFamily method [Direct Write]","GetFontFamily method [Direct Write]","IDWriteFontCollection2 interface","directwrite.idwritefontcollection2_getfontfamily","dwrite_3/IDWriteFontCollection2::GetFontFamily"]
tech.root: DirectWrite
ms.date: 09/12/2019
ms.keywords: IDWriteFontCollection2 interface [Direct Write],GetFontFamily method, IDWriteFontCollection2.GetFontFamily, IDWriteFontCollection2::GetFontFamily, GetFontFamily, GetFontFamily method [Direct Write], GetFontFamily method [Direct Write],IDWriteFontCollection2 interface, directwrite.idwritefontcollection2_getfontfamily, dwrite_3/IDWriteFontCollection2::GetFontFamily
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
 - IDWriteFontCollection2::GetFontFamily
 - dwrite_3/IDWriteFontCollection2::GetFontFamily
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
 - IDWriteFontCollection2::GetFontFamily
---

## -description

Creates a font family object, given a zero-based font family index.

## -parameters

### -param index

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Zero-based index of the font family.

### -param fontFamily [out]

Type: **[IDWriteFontFamily2](./nn-dwrite_3-idwritefontfamily2.md)\*\***

The address of a pointer to an [IDWriteFontFamily2](./nn-dwrite_3-idwritefontfamily2.md) interface. On successful completion, the function sets the pointer to a newly created font family object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
