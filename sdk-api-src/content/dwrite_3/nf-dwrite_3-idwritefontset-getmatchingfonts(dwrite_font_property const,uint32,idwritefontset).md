---
UID: NF:dwrite_3.IDWriteFontSet.GetMatchingFonts(DWRITE_FONT_PROPERTY const,UINT32,IDWriteFontSet)
title: IDWriteFontSet::GetMatchingFonts(DWRITE_FONT_PROPERTY const,UINT32,IDWriteFontSet)
author: windows-sdk-content
description: Returns a subset of fonts filtered by the given properties.
old-location: directwrite\idwritefontset_getmatchingfonts_1.htm
tech.root: DirectWrite
ms.assetid: 3282d528-9997-ee8f-c001-34650551f0e5
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetMatchingFonts, GetMatchingFonts method [Direct Write], GetMatchingFonts method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetMatchingFonts method, IDWriteFontSet.GetMatchingFonts, IDWriteFontSet.GetMatchingFonts(DWRITE_FONT_PROPERTY const,UINT32,IDWriteFontSet), IDWriteFontSet::GetMatchingFonts, IDWriteFontSet::GetMatchingFonts(DWRITE_FONT_PROPERTY const,UINT32,IDWriteFontSet), directwrite.idwritefontset_getmatchingfonts_1, dwrite_3/IDWriteFontSet::GetMatchingFonts
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDWriteFontSet.GetMatchingFonts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite_3.h
: 
- IDWriteFontSet.GetMatchingFonts
: 
---

# IDWriteFontSet::GetMatchingFonts(DWRITE_FONT_PROPERTY const,UINT32,IDWriteFontSet)


## -description


Returns a subset of fonts filtered by the given properties.


## -parameters




### -param properties [in]

Type: <b>const <a href="https://msdn.microsoft.com/C169B175-74FD-423A-8E0A-DC50314D75E6">DWRITE_FONT_PROPERTY</a>*</b>

List of properties to filter using.


### -param propertyCount

Type: <b>UINT32</b>

The number of properties to filter.


### -param filteredSet [out]

Type: <b><a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>**</b>

The subset of fonts that match the properties, or nullptr on failure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If no fonts matched the filter, the subset will be empty (GetFontCount returns 0), but the function does not return an error. The subset will
     always be equal to or less than the original set. If you only want to filter out remote fonts, you may pass null in properties and zero in propertyCount.
     




## -see-also




<a href="https://msdn.microsoft.com/0178f248-8dc0-c0ee-63c1-8db3f6ef94c3">IDWriteFontSet</a>
 

 

