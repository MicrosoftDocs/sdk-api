---
UID: NF:dwrite_3.IDWriteFontSet1.GetFontLocality
title: IDWriteFontSet1::GetFontLocality
description: Retrieves the locality of a single item.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","GetFontLocality method","IDWriteFontSet1.GetFontLocality","IDWriteFontSet1::GetFontLocality","GetFontLocality","GetFontLocality method [Direct Write]","GetFontLocality method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_getfontfacelocality","dwrite_3/IDWriteFontSet1::GetFontLocality"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],GetFontLocality method, IDWriteFontSet1.GetFontLocality, IDWriteFontSet1::GetFontLocality, GetFontLocality, GetFontLocality method [Direct Write], GetFontLocality method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_getfontfacelocality, dwrite_3/IDWriteFontSet1::GetFontLocality
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
 - IDWriteFontSet1::GetFontLocality
 - dwrite_3/IDWriteFontSet1::GetFontLocality
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
 - IDWriteFontSet1::GetFontLocality
---

## -description

Retrieves the locality of a single item.

## -parameters

### -param listIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Zero-based index of the font item in the set.

## -returns

Type: **[DWRITE_LOCALITY](./ne-dwrite_3-dwrite_locality.md)**

A value indicating the locality.

## -remarks

The locality enumeration. For fully local files, the result will always be **DWRITE_LOCALITY_LOCAL**. For downloadable files, the result depends on how much of the file has been downloaded.

## -see-also
