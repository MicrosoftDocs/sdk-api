---
UID: NF:dwrite_3.IDWriteTextFormat3.SetFontAxisValues
title: IDWriteTextFormat3::SetFontAxisValues
description: Sets values for the font axes of the format.
helpviewer_keywords: ["IDWriteTextFormat3 interface [Direct Write]","SetFontAxisValues method","IDWriteTextFormat3.SetFontAxisValues","IDWriteTextFormat3::SetFontAxisValues","SetFontAxisValues","SetFontAxisValues method [Direct Write]","SetFontAxisValues method [Direct Write]","IDWriteTextFormat3 interface","directwrite.idwritetextformat3_setfontaxisvalues","dwrite_3/IDWriteTextFormat3::SetFontAxisValues"]
tech.root: DirectWrite
ms.date: 09/17/2019
ms.keywords: IDWriteTextFormat3 interface [Direct Write],SetFontAxisValues method, IDWriteTextFormat3.SetFontAxisValues, IDWriteTextFormat3::SetFontAxisValues, SetFontAxisValues, SetFontAxisValues method [Direct Write], SetFontAxisValues method [Direct Write],IDWriteTextFormat3 interface, directwrite.idwritetextformat3_setfontaxisvalues, dwrite_3/IDWriteTextFormat3::SetFontAxisValues
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
 - IDWriteTextFormat3::SetFontAxisValues
 - dwrite_3/IDWriteTextFormat3::SetFontAxisValues
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
 - IDWriteTextFormat3::SetFontAxisValues
---

## -description

Sets values for the font axes of the format.

## -parameters

### -param fontAxisValues

Type: **[DWRITE_FONT_AXIS_VALUE](./ns-dwrite_3-dwrite_font_axis_value.md) const \***

A pointer to an array containing a list of font axis values. The array should be the size (the number of elements) indicated by the *fontAxisValueCount* argument.

### -param fontAxisValueCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of font axis values contained in the *fontAxisValues* array.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

## -remarks

## -see-also
