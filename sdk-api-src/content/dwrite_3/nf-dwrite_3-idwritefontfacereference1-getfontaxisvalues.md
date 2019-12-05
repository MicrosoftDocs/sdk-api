---
UID: NF:dwrite_3.IDWriteFontFaceReference1.GetFontAxisValues
title: IDWriteFontFaceReference1::GetFontAxisValues
description: Retrieves the list of font axis values specified by the reference.
tech.root: DirectWrite
ms.date: 09/13/2019
ms.keywords: IDWriteFontFaceReference1 interface [Direct Write],GetFontAxisValues method, IDWriteFontFaceReference1.GetFontAxisValues, IDWriteFontFaceReference1::GetFontAxisValues, GetFontAxisValues, GetFontAxisValues method [Direct Write], GetFontAxisValues method [Direct Write],IDWriteFontFaceReference1 interface, directwrite.idwritefontfacereference1_getfontaxisvalues, dwrite_3/IDWriteFontFaceReference1::GetFontAxisValues
ms.topic: method
f1_keywords:
- dwrite_3/IDWriteFontFaceReference1.GetFontAxisValues
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
- IDWriteFontFaceReference1::GetFontAxisValues
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the list of font axis values specified by the reference.

## -parameters

### -param fontAxisValues [out]

Type: **[DWRITE_FONT_AXIS_VALUE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)\***

A pointer to an array of **DWRITE_FONT_AXIS_VALUE** structures into which **GetFontAxisValues** writes the list of font axis values. You're responsible for managing the size and the lifetime of this array. Call [GetFontAxisValueCount](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontfacereference1-getfontaxisvaluecount) to determine the size of array to allocate.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The maximum number of font axis values to write into the memory block pointed to by `fontAxisValues`.

## -returns

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_INVALIDARG|`fontAxisValueCount` doesn't match the value returned by **GetFontAxisValueCount**.|

## -remarks

## Examples

Follow the same general pattern as shown in the code example for [IDWriteFontFace5::GetFontAxisValues](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontface5-getfontaxisvalues).

## -see-also
