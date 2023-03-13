---
UID: NF:dwrite.IDWriteFontFamily.GetFamilyNames
title: IDWriteFontFamily::GetFamilyNames (dwrite.h)
description: Creates a localized strings object that contains the family names for the font family, indexed by locale name. (IDWriteFontFamily.GetFamilyNames)
helpviewer_keywords: ["GetFamilyNames","GetFamilyNames method [Direct Write]","GetFamilyNames method [Direct Write]","IDWriteFontFamily interface","IDWriteFontFamily interface [Direct Write]","GetFamilyNames method","IDWriteFontFamily.GetFamilyNames","IDWriteFontFamily::GetFamilyNames","directwrite.IDWriteFontFamily_GetFamilyNames","dwrite/IDWriteFontFamily::GetFamilyNames"]
old-location: directwrite\IDWriteFontFamily_GetFamilyNames.htm
tech.root: DirectWrite
ms.assetid: 89b36a28-c8c7-42aa-89a6-7d8f5ddae3fa
ms.date: 12/05/2018
ms.keywords: GetFamilyNames, GetFamilyNames method [Direct Write], GetFamilyNames method [Direct Write],IDWriteFontFamily interface, IDWriteFontFamily interface [Direct Write],GetFamilyNames method, IDWriteFontFamily.GetFamilyNames, IDWriteFontFamily::GetFamilyNames, directwrite.IDWriteFontFamily_GetFamilyNames, dwrite/IDWriteFontFamily::GetFamilyNames
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
 - IDWriteFontFamily::GetFamilyNames
 - dwrite/IDWriteFontFamily::GetFamilyNames
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
 - IDWriteFontFamily.GetFamilyNames
---

# IDWriteFontFamily::GetFamilyNames


## -description

 Creates a localized strings object that contains the family names for the font family, indexed by locale name.

## -parameters

### -param names [out]

Type: <b><a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a>**</b>

The address of a pointer to the newly created <a href="/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings">IDWriteLocalizedStrings</a> object.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following code example shows how to get the font family name from a <a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily">IDWriteFontFamily</a> object.


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

## -see-also

<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily">IDWriteFontFamily</a>

