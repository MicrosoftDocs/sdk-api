---
UID: NF:dwrite_3.IDWriteFontFaceReference1.GetFontAxisValues
title: IDWriteFontFaceReference1::GetFontAxisValues
description: Retrieves the list of font axis values specified by the reference.
helpviewer_keywords: ["IDWriteFontFaceReference1 interface [Direct Write]","GetFontAxisValues method","IDWriteFontFaceReference1.GetFontAxisValues","IDWriteFontFaceReference1::GetFontAxisValues","GetFontAxisValues","GetFontAxisValues method [Direct Write]","GetFontAxisValues method [Direct Write]","IDWriteFontFaceReference1 interface","directwrite.idwritefontfacereference1_getfontaxisvalues","dwrite_3/IDWriteFontFaceReference1::GetFontAxisValues"]
tech.root: DirectWrite
ms.date: 09/13/2019
ms.keywords: IDWriteFontFaceReference1 interface [Direct Write],GetFontAxisValues method, IDWriteFontFaceReference1.GetFontAxisValues, IDWriteFontFaceReference1::GetFontAxisValues, GetFontAxisValues, GetFontAxisValues method [Direct Write], GetFontAxisValues method [Direct Write],IDWriteFontFaceReference1 interface, directwrite.idwritefontfacereference1_getfontaxisvalues, dwrite_3/IDWriteFontFaceReference1::GetFontAxisValues
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
 - IDWriteFontFaceReference1::GetFontAxisValues
 - dwrite_3/IDWriteFontFaceReference1::GetFontAxisValues
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
 - IDWriteFontFaceReference1::GetFontAxisValues
---

## -description

Retrieves the list of font axis values specified by the reference.

## -parameters

### -param fontAxisValues [out]

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md)\***

A pointer to an array of **DWRITE_FONT_AXIS_VALUE** structures into which **GetFontAxisValues** writes the list of font axis values. You're responsible for managing the size and the lifetime of this array. Call [GetFontAxisValueCount](./nf-dwrite_3-idwritefontfacereference1-getfontaxisvaluecount.md) to determine the size of array to allocate.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The maximum number of font axis values to write into the memory block pointed to by `fontAxisValues`.

## -returns

## -remarks

## Examples

Follow the same general pattern as shown in the code example for [IDWriteFontFace5::GetFontAxisValues](./nf-dwrite_3-idwritefontface5-getfontaxisvalues.md).

## -see-also
