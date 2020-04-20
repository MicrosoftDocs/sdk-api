---
UID: NF:dwrite_3.IDWriteFontSet3.GetFontSourceName
title: IDWriteFontSet3::GetFontSourceName
description: Copies the font source name (for the specified font) into an output array.helpviewer_keywords: ["IDWriteFontSet3 interface [Direct Write]","GetFontSourceName method","IDWriteFontSet3.GetFontSourceName","IDWriteFontSet3::GetFontSourceName","GetFontSourceName","GetFontSourceName method [Direct Write]","GetFontSourceName method [Direct Write]","IDWriteFontSet3 interface","directwrite.idwritefontset3_getfontsourcename","dwrite_3/IDWriteFontSet3::GetFontSourceName"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet3 interface [Direct Write],GetFontSourceName method, IDWriteFontSet3.GetFontSourceName, IDWriteFontSet3::GetFontSourceName, GetFontSourceName, GetFontSourceName method [Direct Write], GetFontSourceName method [Direct Write],IDWriteFontSet3 interface, directwrite.idwritefontset3_getfontsourcename, dwrite_3/IDWriteFontSet3::GetFontSourceName
f1_keywords:
- dwrite_3/IDWriteFontSet3.GetFontSourceName
dev_langs:
- c++
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
- IDWriteFontSet3::GetFontSourceName
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Copies the font source name (for the specified font) into an output array.

## -parameters

### -param listIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Zero-based index of the font.

### -param stringBuffer [out]

Type: **[WCHAR](/windows/win32/winprog/windows-data-types)\***

Character array that receives the string. Call [GetFontSourceNameLength](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset3-getfontsourcenamelength) to determine the size of array to allocate.

### -param stringBufferSize

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Size of the array in characters. The size must include space for the terminating null character.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also

[GetFontSourceNameLength](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontset3-getfontsourcenamelength)
