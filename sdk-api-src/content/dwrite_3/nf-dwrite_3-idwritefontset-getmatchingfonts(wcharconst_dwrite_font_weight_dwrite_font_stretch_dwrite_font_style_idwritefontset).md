---
UID: NF:dwrite_3.IDWriteFontSet.GetMatchingFonts(WCHARconst,DWRITE_FONT_WEIGHT,DWRITE_FONT_STRETCH,DWRITE_FONT_STYLE,IDWriteFontSet)
title: IDWriteFontSet::GetMatchingFonts(WCHAR const,DWRITE_FONT_WEIGHT,DWRITE_FONT_STRETCH,DWRITE_FONT_STYLE,IDWriteFontSet) (dwrite_3.h)
description: Returns a subset of fonts filtered by the given properties.
helpviewer_keywords: ["GetMatchingFonts","GetMatchingFonts method [Direct Write]","GetMatchingFonts method [Direct Write]","IDWriteFontSet interface","IDWriteFontSet interface [Direct Write]","GetMatchingFonts method","IDWriteFontSet.GetMatchingFonts","IDWriteFontSet.GetMatchingFonts(WCHAR const","DWRITE_FONT_WEIGHT","DWRITE_FONT_STRETCH","DWRITE_FONT_STYLE","IDWriteFontSet)","IDWriteFontSet::GetMatchingFonts","IDWriteFontSet::GetMatchingFonts(WCHAR const","DWRITE_FONT_WEIGHT","DWRITE_FONT_STRETCH","DWRITE_FONT_STYLE","IDWriteFontSet)","directwrite.idwritefontset_getmatchingfonts_1","dwrite_3/IDWriteFontSet::GetMatchingFonts"]
old-location: directwrite\idwritefontset_getmatchingfonts_1.htm
tech.root: DirectWrite
ms.assetid: 3282d528-9997-ee8f-c001-34650551f0e5
ms.date: 12/05/2018
ms.keywords: GetMatchingFonts, GetMatchingFonts method [Direct Write], GetMatchingFonts method [Direct Write],IDWriteFontSet interface, IDWriteFontSet interface [Direct Write],GetMatchingFonts method, IDWriteFontSet.GetMatchingFonts, IDWriteFontSet.GetMatchingFonts(WCHAR const,DWRITE_FONT_WEIGHT,DWRITE_FONT_STRETCH,DWRITE_FONT_STYLE,IDWriteFontSet), IDWriteFontSet::GetMatchingFonts, IDWriteFontSet::GetMatchingFonts(WCHAR const,DWRITE_FONT_WEIGHT,DWRITE_FONT_STRETCH,DWRITE_FONT_STYLE,IDWriteFontSet), directwrite.idwritefontset_getmatchingfonts_1, dwrite_3/IDWriteFontSet::GetMatchingFonts
f1_keywords:
- dwrite_3/IDWriteFontSet.GetMatchingFonts
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
- IDWriteFontSet.GetMatchingFonts
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteFontSet::GetMatchingFonts(WCHAR const,DWRITE_FONT_WEIGHT,DWRITE_FONT_STRETCH,DWRITE_FONT_STYLE,IDWriteFontSet)


## -description


Returns a subset of fonts filtered by the given properties.


## -parameters




### -param familyName

The font family name.


### -param fontWeight

The font weight.


### -param fontStretch

The font stretch value.


### -param fontStyle

The font style.


### -param filteredSet [out]

Type: <b><a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>**</b>

The subset of fonts that match the properties, or nullptr on failure.




## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If no fonts matched the filter, the subset will be empty (GetFontCount returns 0), but the function does not return an error. The subset will
     always be equal to or less than the original set. If you only want to filter out remote fonts, you may pass null in properties and zero in propertyCount.
     




## -see-also




<a href="/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset">IDWriteFontSet</a>
 

 

