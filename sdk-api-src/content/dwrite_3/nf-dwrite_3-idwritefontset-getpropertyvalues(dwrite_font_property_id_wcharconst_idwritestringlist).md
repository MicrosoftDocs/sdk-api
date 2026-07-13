---
UID: NF:dwrite_3.IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHARconst,IDWriteStringList)
title: IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList) (dwrite_3.h)
description: Returns the property values of a specific font item index. (overload 1/3)
helpviewer_keywords: ["GetPropertyValues","GetPropertyValues method [Direct Write]","GetPropertyValues method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","GetPropertyValues method","IDWriteFontSet.GetPropertyValues","IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID","WCHAR const","IDWriteStringList)","IDWriteFontSet::GetPropertyValues","IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID","WCHAR const","IDWriteStringList)","directwrite.idwritefontset_getpropertyvalues_1","dwrite_3/IDWriteFontSet::GetPropertyValues"]
old-location: directwrite\idwritefontset_getpropertyvalues_1.htm
tech.root: DirectWrite
ms.assetid: 4523d5a6-9d5f-61ac-a47f-810fef1522a9
ms.date: 09/10/2025
req.header: dwrite_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Dwrite.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDWriteFontSet::GetPropertyValues
 - dwrite_3/IDWriteFontSet::GetPropertyValues
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontSet.GetPropertyValues
---

## -description

Returns all unique property values in the set, which can be used for purposes such as displaying a family list or tag cloud. Values are returned in priority order according to the language list, such that if a font contains more than one localized name, then the preferred one is returned.

## -parameters

### -param propertyID

Type: <b><a href="/windows/desktop/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id">DWRITE_FONT_PROPERTY_ID</a></b>

Font property of interest.

### -param preferredLocaleNames

Type: **[WCHAR](/windows/win32/winprog/windows-data-types) const \***

The preferred locale names to query as a list of semicolon-delimited names in preferred order. When a particular string (such as font family) has more than one localized name, then the first match is returned. If the first match doesn't exist, then the second match is returned, and so on. For example, "ja-jp;en-us".

### -param values

Type: \[out\] <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

Receives a pointer to the newly created localized strings object; or `nullptr` on failure or non-existent property.

## -returns

Type: **[HRESULT](/windows/win32/com/structure-of-com-error-codes)**

If this method succeeds, then it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>
