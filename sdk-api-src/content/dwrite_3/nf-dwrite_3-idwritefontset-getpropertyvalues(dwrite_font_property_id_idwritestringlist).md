---
UID: NF:dwrite_3.IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID,IDWriteStringList)
title: IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,IDWriteStringList) (dwrite_3.h)
description: Returns the property values of a specific font item index. (overload 2/3)
helpviewer_keywords: ["GetPropertyValues","GetPropertyValues method [Direct Write]","GetPropertyValues method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","GetPropertyValues method","IDWriteFontSet.GetPropertyValues","IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID","IDWriteStringList)","IDWriteFontSet::GetPropertyValues","IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID","IDWriteStringList)","directwrite.idwritefontset_getpropertyvalues_1","dwrite_3/IDWriteFontSet::GetPropertyValues"]
old-location: directwrite\idwritefontset_getpropertyvalues_1.htm
tech.root: DirectWrite
ms.assetid: 4523d5a6-9d5f-61ac-a47f-810fef1522a9
ms.date: 09/10/2025
ms.keywords: GetPropertyValues, GetPropertyValues method [Direct Write], GetPropertyValues method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetPropertyValues method, IDWriteFontSet.GetPropertyValues, IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID,IDWriteStringList), IDWriteFontSet::GetPropertyValues, IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,IDWriteStringList), directwrite.idwritefontset_getpropertyvalues_1, dwrite_3/IDWriteFontSet::GetPropertyValues
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

# IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,IDWriteStringList)


## -description

Returns the property values of a specific font item index.

## -parameters

### -param propertyID

Type: <b><a href="/windows/desktop/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id">DWRITE_FONT_PROPERTY_ID</a></b>

Font property of interest.

### -param values [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

Receives a pointer to the newly created localized strings object, or nullptr on failure or non-existent property.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>
