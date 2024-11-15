---
UID: NF:dwrite_3.IDWriteFontResource.GetAxisValueNames
title: IDWriteFontResource::GetAxisValueNames
description: Retrieves the localized names of specific values for a font axis.
helpviewer_keywords: ["IDWriteFontResource interface [Direct Write]","GetAxisValueNames method","IDWriteFontResource.GetAxisValueNames","IDWriteFontResource::GetAxisValueNames","GetAxisValueNames","GetAxisValueNames method [Direct Write]","GetAxisValueNames method [Direct Write]","IDWriteFontResource interface","directwrite.idwritefontresource_getaxisvaluenames","dwrite_3/IDWriteFontResource::GetAxisValueNames"]
tech.root: DirectWrite
ms.date: 09/13/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetAxisValueNames method, IDWriteFontResource.GetAxisValueNames, IDWriteFontResource::GetAxisValueNames, GetAxisValueNames, GetAxisValueNames method [Direct Write], GetAxisValueNames method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getaxisvaluenames, dwrite_3/IDWriteFontResource::GetAxisValueNames
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
 - IDWriteFontResource::GetAxisValueNames
 - dwrite_3/IDWriteFontResource::GetAxisValueNames
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
 - IDWriteFontResource::GetAxisValueNames
---

## -description

Retrieves the localized names of specific values for a font axis.

## -parameters

### -param axisIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Font axis, from 0 to [GetFontAxisCount](./nf-dwrite_3-idwritefontresource-getfontaxiscount.md) minus 1.

### -param axisValueIndex

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

Value index, from 0 to [GetAxisValueNameCount](./nf-dwrite_3-idwritefontresource-getaxisvaluenamecount.md) minus 1.

### -param fontAxisRange [out]

Type: **[DWRITE_FONT_AXIS_RANGE](./ns-dwrite_3-dwrite_font_axis_range.md)\***

Range of the named value.

### -param names [out]

Type: **[IDWriteLocalizedStrings](../dwrite/nn-dwrite-idwritelocalizedstrings.md)\*\***

The address of a pointer to an [IDWriteLocalizedStrings](../dwrite/nn-dwrite-idwritelocalizedstrings.md) interface. On successful completion, the function sets the pointer to a newly created localized strings object.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

The font author may not have supplied names for some font axis values. The localized strings will be empty in that case. The range may be a single point, where *minValue* == *maxValue*. All ranges are in ascending order by *axisValueIndex*.

## -see-also
