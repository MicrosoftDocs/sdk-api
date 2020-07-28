---
UID: NF:dwrite_3.IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHARconst,IDWriteStringList)
title: IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList) (dwrite_3.h)
description: Returns the property values of a specific font item index.
helpviewer_keywords: ["GetPropertyValues","GetPropertyValues method [Direct Write]","GetPropertyValues method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","GetPropertyValues method","IDWriteFontSet.GetPropertyValues","IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID","WCHAR const","IDWriteStringList)","IDWriteFontSet::GetPropertyValues","IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID","WCHAR const","IDWriteStringList)","directwrite.idwritefontset_getpropertyvalues_1","dwrite_3/IDWriteFontSet::GetPropertyValues"]
old-location: directwrite\idwritefontset_getpropertyvalues_1.htm
tech.root: DirectWrite
ms.assetid: 4523d5a6-9d5f-61ac-a47f-810fef1522a9
ms.date: 12/05/2018
ms.keywords: GetPropertyValues, GetPropertyValues method [Direct Write], GetPropertyValues method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetPropertyValues method, IDWriteFontSet.GetPropertyValues, IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList), IDWriteFontSet::GetPropertyValues, IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList), directwrite.idwritefontset_getpropertyvalues_1, dwrite_3/IDWriteFontSet::GetPropertyValues
f1_keywords:
- dwrite_3/IDWriteFontSet.GetPropertyValues
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteFontSet.GetPropertyValues
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList)


## -description


Returns the property values of a specific font item index.


## -parameters




### -param propertyID

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/dwrite_3/ne-dwrite_3-dwrite_font_property_id">DWRITE_FONT_PROPERTY_ID</a></b>

Font property of interest.



### -param preferredLocaleNames

The preferred locale names to query.


### -param values [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

Receives a pointer to the newly created localized strings object, or nullptr on failure or non-existent property.




## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>
 

 

