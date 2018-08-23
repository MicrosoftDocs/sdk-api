---
UID: NF:dwrite_3.IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList)
title: IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList)
author: windows-sdk-content
description: Returns the property values of a specific font item index.
old-location: directwrite\idwritefontset_getpropertyvalues_1.htm
old-project: DirectWrite
ms.assetid: 4523d5a6-9d5f-61ac-a47f-810fef1522a9
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetPropertyValues, GetPropertyValues method [Direct Write], GetPropertyValues method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetPropertyValues method, IDWriteFontSet.GetPropertyValues, IDWriteFontSet.GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList), IDWriteFontSet::GetPropertyValues, IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList), directwrite.idwritefontset_getpropertyvalues_1, dwrite_3/IDWriteFontSet::GetPropertyValues
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite_3.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontSet.GetPropertyValues
product: Windows
targetos: Windows
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDWriteFontSet::GetPropertyValues(DWRITE_FONT_PROPERTY_ID,WCHAR const,IDWriteStringList)


## -description


Returns the property values of a specific font item index.


## -parameters




### -param propertyID




### -param preferredLocaleNames




### -param values [out]

Type: <b><a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>**</b>

Receives a pointer to the newly created localized strings object, or nullptr on failure or non-existent property.


#### - exists [out]

Type: <b>BOOL*</b>

Receives the value TRUE if the font contains the specified property identifier or FALSE if not.


#### - listIndex

Type: <b>UINT32</b>

Zero-based index of the font.


#### - propertyId

Type: <b><a href="https://msdn.microsoft.com/9743F54F-B661-444F-8579-DE03B0891F9C">DWRITE_FONT_PROPERTY_ID</a></b>

Font property of interest.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>
 

 

