---
UID: NF:dwrite_3.IDWriteFontSet1.GetFontAxisRanges
title: IDWriteFontSet1::GetFontAxisRanges
description: Retrieves all axis ranges in the font set; the union of all contained items.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","GetFontAxisRanges method","IDWriteFontSet1.GetFontAxisRanges","IDWriteFontSet1::GetFontAxisRanges","GetFontAxisRanges","GetFontAxisRanges method [Direct Write]","GetFontAxisRanges method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_getfontaxisranges","dwrite_3/IDWriteFontSet1::GetFontAxisRanges"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],GetFontAxisRanges method, IDWriteFontSet1.GetFontAxisRanges, IDWriteFontSet1::GetFontAxisRanges, GetFontAxisRanges, GetFontAxisRanges method [Direct Write], GetFontAxisRanges method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_getfontaxisranges, dwrite_3/IDWriteFontSet1::GetFontAxisRanges
f1_keywords:
- dwrite_3/IDWriteFontSet1.GetFontAxisRanges
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: 
---

STDMETHOD(GetFontAxisRanges)(
    _Out_writes_(maxFontAxisRangeCount) DWRITE_FONT_AXIS_RANGE* fontAxisRanges,
    UINT32 maxFontAxisRangeCount,
    ) PURE;

## -description

Retrieves all axis ranges in the font set; the union of all contained items.

## -parameters

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