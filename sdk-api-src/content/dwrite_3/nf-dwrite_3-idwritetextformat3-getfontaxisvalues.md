---
UID: NF:dwrite_3.IDWriteTextFormat3.GetFontAxisValues
title: IDWriteTextFormat3::GetFontAxisValues
description: Retrieves the list of font axis values on the format.
helpviewer_keywords: ["IDWriteTextFormat3 interface [Direct Write]","GetFontAxisValues method","IDWriteTextFormat3.GetFontAxisValues","IDWriteTextFormat3::GetFontAxisValues","GetFontAxisValues","GetFontAxisValues method [Direct Write]","GetFontAxisValues method [Direct Write]","IDWriteTextFormat3 interface","directwrite.idwritetextformat3_getfontaxisvalues","dwrite_3/IDWriteTextFormat3::GetFontAxisValues"]
tech.root: DirectWrite
ms.date: 09/10/2025
ms.keywords: IDWriteTextFormat3 interface [Direct Write],GetFontAxisValues method, IDWriteTextFormat3.GetFontAxisValues, IDWriteTextFormat3::GetFontAxisValues, GetFontAxisValues, GetFontAxisValues method [Direct Write], GetFontAxisValues method [Direct Write],IDWriteTextFormat3 interface, directwrite.idwritetextformat3_getfontaxisvalues, dwrite_3/IDWriteTextFormat3::GetFontAxisValues
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
 - IDWriteTextFormat3::GetFontAxisValues
 - dwrite_3/IDWriteTextFormat3::GetFontAxisValues
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
 - IDWriteTextFormat3::GetFontAxisValues
---

## -description

Retrieves the list of font axis values on the format.

## -parameters

### -param fontAxisValues [out]

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md)\***

A pointer to an array of **DWRITE_FONT_AXIS_VALUE** structures into which **GetFontAxisValues** writes the list of font axis values. You're responsible for managing the size and the lifetime of this array. Call [GetFontAxisValueCount](./nf-dwrite_3-idwritetextformat3-getfontaxisvaluecount.md) to determine the size of array to allocate.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The maximum number of font axis values to write into the memory block pointed to by `fontAxisValues`.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
