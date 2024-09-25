---
UID: NF:dwrite_3.IDWriteFontSet1.GetFontAxisRanges(UINT32,DWRITE_FONT_AXIS_RANGE,UINT32,UINT32)
title: IDWriteFontSet1::GetFontAxisRanges
description: Retrieves the axis ranges of a single item.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","GetFontAxisRanges method","IDWriteFontSet1.GetFontAxisRanges","IDWriteFontSet1::GetFontAxisRanges","GetFontAxisRanges","GetFontAxisRanges method [Direct Write]","GetFontAxisRanges method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_getfontaxisranges","dwrite_3/IDWriteFontSet1::GetFontAxisRanges"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],GetFontAxisRanges method, IDWriteFontSet1.GetFontAxisRanges, IDWriteFontSet1::GetFontAxisRanges, GetFontAxisRanges, GetFontAxisRanges method [Direct Write], GetFontAxisRanges method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_getfontaxisranges, dwrite_3/IDWriteFontSet1::GetFontAxisRanges
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
 - IDWriteFontSet1::GetFontAxisRanges
 - dwrite_3/IDWriteFontSet1::GetFontAxisRanges
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
 - IDWriteFontSet1::GetFontAxisRanges
---

## -description

Retrieves the axis ranges of a single item.

## -parameters

### -param listIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Zero-based index of the font in the set.

### -param fontAxisRanges [out]

Type: **[DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md)\***

List of axis value ranges to retrieve.

### -param maxFontAxisRangeCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of axis value ranges to retrieve.

### -param actualFontAxisRangeCount [out]

Type: **[UINT32](/windows/win32/winprog/windows-data-types)\***

The actual number of axis ranges written or needed.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_NOT_SUFFICIENT_BUFFER|The buffer is too small, with *actualFontAxisRangeCount* set to the needed size.|

## -remarks

## -see-also
