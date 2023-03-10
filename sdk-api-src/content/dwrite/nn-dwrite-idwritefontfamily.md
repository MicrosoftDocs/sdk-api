---
UID: NN:dwrite.IDWriteFontFamily
title: IDWriteFontFamily (dwrite.h)
description: Represents a family of related fonts. (IDWriteFontFamily)
helpviewer_keywords: ["IDWriteFontFamily","IDWriteFontFamily interface [Direct Write]","IDWriteFontFamily interface [Direct Write]","described","directwrite.IDWriteFontFamily","dwrite/IDWriteFontFamily"]
old-location: directwrite\IDWriteFontFamily.htm
tech.root: DirectWrite
ms.assetid: 1fce3d62-af4e-4d2b-a3fd-e534b5fcdb13
ms.date: 12/05/2018
ms.keywords: IDWriteFontFamily, IDWriteFontFamily interface [Direct Write], IDWriteFontFamily interface [Direct Write],described, directwrite.IDWriteFontFamily, dwrite/IDWriteFontFamily
req.header: dwrite.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
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
 - IDWriteFontFamily
 - dwrite/IDWriteFontFamily
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
 - IDWriteFontFamily
---

# IDWriteFontFamily interface


## -description

Represents a family of related fonts.

## -inheritance

The <b>IDWriteFontFamily</b> interface inherits from <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontlist">IDWriteFontList</a>. <b>IDWriteFontFamily</b> also has these types of members:

## -remarks

A font family is a set of fonts that share the same family name, such as "Times New Roman", but that differ in features. These feature differences include style, such as italic, and weight, such as bold. 

The following illustration shows examples of fonts that are members of the "Times New Roman" font family.

<img alt="Illustration of italic, bold, and bold italic text from the Times New Roman font family" src="./images/FontFamily_for_TimesNewRoman.png"/>
An <b>IDWriteFontFamily</b> object can be retrieved from a font collection using the  <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefont-getfontfamily">IDWriteFontCollection::GetFontFamily</a> method shown in the following example.  <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontcollection-getfontfamily">GetFontFamily</a> takes a <b>UINT32</b> index and returns the font family for the font at that index.


```cpp
IDWriteFontFamily* pFontFamily = NULL;

// Get the font family.
if (SUCCEEDED(hr))
{
    hr = pFontCollection->GetFontFamily(i, &pFontFamily);
}

```


The font family name is used to specify the font family for text layout and text format objects.  You can get a list of localized font family names from an <b>IDWriteFontFamily</b> object in the form of an <a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a> object by using the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames">IDWriteFontFamily::GetFamilyNames</a> method, as shown in the following code.


```cpp
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}

```

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontlist">IDWriteFontList</a>

