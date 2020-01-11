---
UID: NF:dwrite_3.IDWriteFontResource.GetFontAxisRanges
title: IDWriteFontResource::GetFontAxisRanges
description: Retrieves the value ranges of each axis.
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetFontAxisRanges method, IDWriteFontResource.GetFontAxisRanges, IDWriteFontResource::GetFontAxisRanges, GetFontAxisRanges, GetFontAxisRanges method [Direct Write], GetFontAxisRanges method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getfontaxisranges, dwrite_3/IDWriteFontResource::GetFontAxisRanges
f1_keywords:
- dwrite_3/IDWriteFontResource.GetFontAxisRanges
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
- IDWriteFontResource::GetFontAxisRanges
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the value ranges of each axis.

## -parameters

### -param fontAxisRanges [out]

Type: **[DWRITE_FONT_AXIS_RANGE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_range)\***

A pointer to an array of **DWRITE_FONT_AXIS_RANGE** structures into which **GetFontAxisRanges** writes the list of font axis value ranges. You're responsible for managing the size and the lifetime of this array. Call [GetFontAxisCount](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-getfontaxiscount) to determine the size of array to allocate.

### -param fontAxisRangeCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The maximum number of font axis value ranges to write into the memory block pointed to by `fontAxisRanges`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_INVALIDARG|`fontAxisValueCount` doesn't match the value returned by **GetFontAxisCount**.|

## -remarks

A non-varying axis has an empty range (*minValue* == *maxValue*).

## -see-also
