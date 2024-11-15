---
UID: NF:dwrite_3.IDWriteFontSet1.GetFilteredFontIndices
title: IDWriteFontSet1::GetFilteredFontIndices
description: Retrieves all the item indices, filtered by the given properties.
helpviewer_keywords: ["IDWriteFontSet1 interface [Direct Write]","GetFilteredFontIndices method","IDWriteFontSet1.GetFilteredFontIndices","IDWriteFontSet1::GetFilteredFontIndices","GetFilteredFontIndices","GetFilteredFontIndices method [Direct Write]","GetFilteredFontIndices method [Direct Write]","IDWriteFontSet1 interface","directwrite.idwritefontset1_getfilteredfontindices","dwrite_3/IDWriteFontSet1::GetFilteredFontIndices"]
tech.root: DirectWrite
ms.date: 09/16/2019
ms.keywords: IDWriteFontSet1 interface [Direct Write],GetFilteredFontIndices method, IDWriteFontSet1.GetFilteredFontIndices, IDWriteFontSet1::GetFilteredFontIndices, GetFilteredFontIndices, GetFilteredFontIndices method [Direct Write], GetFilteredFontIndices method [Direct Write],IDWriteFontSet1 interface, directwrite.idwritefontset1_getfilteredfontindices, dwrite_3/IDWriteFontSet1::GetFilteredFontIndices
f1_keywords:
- dwrite_3/IDWriteFontSet1.GetFilteredFontIndices
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
- IDWriteFontSet1::GetFilteredFontIndices
targetos: Windows
req.typenames: 
req.redist: 
---

## -description

Retrieves all the item indices, filtered by the given properties.

## -parameters

### -param properties

Type: **[DWRITE_FONT_PROPERTY](./ns-dwrite_3-dwrite_font_property.md) const \***

List of properties to filter by.

### -param propertyCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of properties to filter.

### -param selectAnyProperty

Type: **[BOOL](/windows/win32/winprog/windows-data-types)**

`true` if **GetFilteredFontIndices** should select any property; `false` if it should select the intersection of them all.

### -param indices [out]

Type: **[UINT32](/windows/win32/winprog/windows-data-types)\***

An ascending array of indices, in the range 0 to [IDwriteFontSet::GetFontCount](./nf-dwrite_3-idwritefontset-getfontcount.md) minus 1.

### -param maxIndexCount

Type: **[UINT32](/windows/win32/winprog/windows-data-types)**

The number of indices.

### -param actualIndexCount [out]

Type: **[UINT32](/windows/win32/winprog/windows-data-types)\***

The actual number of indices written or needed, in the range 0 to [IDwriteFontSet::GetFontCount](./nf-dwrite_3-idwritefontset-getfontcount.md) minus 1.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If the function succeeds, it returns **S_OK**. Otherwise, it returns an [**HRESULT**](/windows/win32/com/structure-of-com-error-codes) [error code](/windows/win32/com/com-error-codes-10).

|Return value|Description|
|-|-|
|E_NOT_SUFFICIENT_BUFFER|The buffer is too small, with *actualIndexCount* set to the needed size. The *actualIndexCount* will always be <= [IDwriteFontSet::GetFontCount](./nf-dwrite_3-idwritefontset-getfontcount.md).|

## -remarks

## -see-also