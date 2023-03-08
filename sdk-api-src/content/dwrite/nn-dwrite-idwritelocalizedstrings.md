---
UID: NN:dwrite.IDWriteLocalizedStrings
title: IDWriteLocalizedStrings (dwrite.h)
description: Represents a collection of strings indexed by locale name.
helpviewer_keywords: ["IDWriteLocalizedStrings","IDWriteLocalizedStrings interface [Direct Write]","IDWriteLocalizedStrings interface [Direct Write]","described","directwrite.IDWriteLocalizedStrings","dwrite/IDWriteLocalizedStrings"]
old-location: directwrite\IDWriteLocalizedStrings.htm
tech.root: DirectWrite
ms.assetid: 37bfc613-4128-45aa-b6b2-6163d44378e4
ms.date: 12/05/2018
ms.keywords: IDWriteLocalizedStrings, IDWriteLocalizedStrings interface [Direct Write], IDWriteLocalizedStrings interface [Direct Write],described, directwrite.IDWriteLocalizedStrings, dwrite/IDWriteLocalizedStrings
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
 - IDWriteLocalizedStrings
 - dwrite/IDWriteLocalizedStrings
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
 - IDWriteLocalizedStrings
---

# IDWriteLocalizedStrings interface


## -description

 Represents a collection of strings indexed by locale name.

## -inheritance

The <b>IDWriteLocalizedStrings</b> interface inherits from the <a href="/windows/win32/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDWriteLocalizedStrings</b> also has these types of members:

## -remarks

The set of strings represented by an <b>IDWriteLocalizedStrings</b> are indexed by a zero based <i>UINT32</i> number that maps to a locale.  The numeric index for a specific locale is retreived by using the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritelocalizedstrings-findlocalename">FindLocaleName</a> method.

A common use for the <b>IDWriteLocalizedStrings</b> interface is to hold a list of localized font family names created by using the <a href="/windows/win32/api/dwrite/nf-dwrite-idwritefontfamily-getfamilynames">IDWriteFontFamily::GetFamilyNames</a> method.  The following example shows how to get the family name for the "en-us" locale.


```cpp
IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily->GetFamilyNames(&pFamilyNames);
}

UINT32 index = 0;
BOOL exists = false;

wchar_t localeName[LOCALE_NAME_MAX_LENGTH];

if (SUCCEEDED(hr))
{
    // Get the default locale for this user.
    int defaultLocaleSuccess = GetUserDefaultLocaleName(localeName, LOCALE_NAME_MAX_LENGTH);

    // If the default locale is returned, find that locale name, otherwise use "en-us".
    if (defaultLocaleSuccess)
    {
        hr = pFamilyNames->FindLocaleName(localeName, &index, &exists);
    }
    if (SUCCEEDED(hr) && !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames->FindLocaleName(L"en-us", &index, &exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;

UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetStringLength(index, &length);
}

// Allocate a string big enough to hold the name.
wchar_t* name = new (std::nothrow) wchar_t[length+1];
if (name == NULL)
{
    hr = E_OUTOFMEMORY;
}

// Get the family name.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames->GetString(index, name, length+1);
}

```

