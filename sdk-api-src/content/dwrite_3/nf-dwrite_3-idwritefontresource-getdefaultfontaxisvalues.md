---
UID: NF:dwrite_3.IDWriteFontResource.GetDefaultFontAxisValues
title: IDWriteFontResource::GetDefaultFontAxisValues
author: windows-sdk-content
description: Retrieves the default values for all axes supported by the font resource.
tech.root: DirectWrite
ms.author: windowssdkdev
ms.date: 09/16/2019
ms.keywords: IDWriteFontResource interface [Direct Write],GetDefaultFontAxisValues method, IDWriteFontResource.GetDefaultFontAxisValues, IDWriteFontResource::GetDefaultFontAxisValues, GetDefaultFontAxisValues, GetDefaultFontAxisValues method [Direct Write], GetDefaultFontAxisValues method [Direct Write],IDWriteFontResource interface, directwrite.idwritefontresource_getdefaultfontaxisvalues, dwrite_3/IDWriteFontResource::GetDefaultFontAxisValues
ms.topic: method
f1_keywords: 
 - "dwrite_3/IDWriteFontResource.GetDefaultFontAxisValues"
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
 - IDWriteFontResource::GetDefaultFontAxisValues
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves the default values for all axes supported by the font resource.

## -parameters

### -param fontAxisValues [out]

Type: **[DWRITE_FONT_AXIS_VALUE](/windows/win32/api/dwrite_3/ns-dwrite_3-dwrite_font_axis_value)\***

A pointer to an array of **DWRITE_FONT_AXIS_VALUE** structures into which **GetDefaultFontAxisValues** writes the list of font axis values. You're responsible for managing the size and the lifetime of this array. Call [GetFontAxisCount](/windows/win32/api/dwrite_3/nf-dwrite_3-idwritefontresource-getfontaxiscount) to determine the size of array to allocate.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The maximum number of font axis values to write into the memory block pointed to by `fontAxisValues`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_INVALIDARG|`fontAxisValueCount` doesn't match the value returned by **GetFontAxisCount**.|

## -remarks

Different font resources may have different defaults. For OpenType 1.8 fonts, these values come from the STAT and fvar tables. For older fonts without a STAT table, weight-width-slant-italic are read from the OS/2 table.

## -see-also
