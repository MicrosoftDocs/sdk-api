---
UID: NN:dwrite.IDWriteFontCollection
title: IDWriteFontCollection
author: windows-sdk-content
description: An object that encapsulates a set of fonts, such as the set of fonts installed on the system, or the set of fonts in a particular directory.
old-location: directwrite\IDWriteFontCollection.htm
tech.root: DirectWrite
ms.assetid: 2ca7e2d3-d66a-4c57-8fbe-15a5232c3506
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteFontCollection, IDWriteFontCollection interface [Direct Write], IDWriteFontCollection interface [Direct Write],described, directwrite.IDWriteFontCollection, dwrite/IDWriteFontCollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteFontCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontCollection interface


## -description


 An object that encapsulates a set of fonts, such as the set of fonts installed on the system, or the set of fonts in a particular directory. The font collection API can be used to discover what font families and fonts are available, and to obtain some metadata about the fonts.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteFontCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteFontCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteFontCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5537988f-aba0-4477-be01-72a5f8e66395">FindFamilyName</a>
</td>
<td align="left" width="63%">
 Finds the font family with the specified family name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/470c63cc-b50f-4b62-98c0-f7ce183bfcfd">GetFontFamily</a>
</td>
<td align="left" width="63%">
 Creates a font family object given a zero-based font family index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/82b6409a-6f6c-4b8d-9c48-916f1f7f3750">GetFontFamilyCount</a>
</td>
<td align="left" width="63%">
 Gets the number of font families in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc3c6cb9-9e98-4d45-bf73-ee625fb17e8c">GetFontFromFontFace</a>
</td>
<td align="left" width="63%">
 Gets the font object that corresponds to the same physical font as the specified font face object. The specified physical font must belong 
     to the font collection.

</td>
</tr>
</table> 


## -remarks



The <a href="https://msdn.microsoft.com/4f5cbea1-9775-4266-aa3c-7c15892d61b1">IDWriteFactory::GetSystemFontCollection</a> method will give you an <b>IDWriteFontCollection</b> object, which encapsulates the set of fonts installed on the system, as shown in the following code example.


```cpp
IDWriteFontCollection* pFontCollection = NULL;

// Get the system font collection.
if (SUCCEEDED(hr))
{
    hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
}

```



<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a> and <a href="https://msdn.microsoft.com/0d687337-8623-4014-967c-f533072e31cc">IDWriteTextLayout</a> both have a <a href="https://msdn.microsoft.com/a94cfca5-3a03-4912-9a33-df705a2265cf">GetFontCollection</a> method that returns the font collection being used by the object.  These interfaces use the system font collection by default, but can use a custom font collection instead.

To determine what fonts are available on the system,  get a reference to the system font collection.  You can then use the <a href="https://msdn.microsoft.com/82b6409a-6f6c-4b8d-9c48-916f1f7f3750">IDWriteFontCollection::GetFontFamilyCount</a> method to determine the number of fonts and loop through the list. The following example enumerates the fonts in the system font collection, and prints the font family names to the console.


```cpp

#include <dwrite.h>
#include <string.h>
#include <stdio.h>
#include <new>

// SafeRelease inline function.
template <class T> inline void SafeRelease(T **ppT)
{
    if (*ppT)
    {
        (*ppT)->Release();
        *ppT = NULL;
    }
}

void wmain()
{
    IDWriteFactory* pDWriteFactory = NULL;

    HRESULT hr = DWriteCreateFactory(
            DWRITE_FACTORY_TYPE_SHARED,
            __uuidof(IDWriteFactory),
            reinterpret_cast<IUnknown**>(&pDWriteFactory)
            );

    IDWriteFontCollection* pFontCollection = NULL;

    // Get the system font collection.
    if (SUCCEEDED(hr))
    {
        hr = pDWriteFactory->GetSystemFontCollection(&pFontCollection);
    }

    UINT32 familyCount = 0;

    // Get the number of font families in the collection.
    if (SUCCEEDED(hr))
    {
        familyCount = pFontCollection->GetFontFamilyCount();
    }

    for (UINT32 i = 0; i < familyCount; ++i)
    {
        IDWriteFontFamily* pFontFamily = NULL;

        // Get the font family.
        if (SUCCEEDED(hr))
        {
            hr = pFontCollection->GetFontFamily(i, &pFontFamily);
        }

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
        if (SUCCEEDED(hr))
        {
            // Print out the family name.
            wprintf(L"%s\n", name);
        }

        SafeRelease(&pFontFamily);
        SafeRelease(&pFamilyNames);

        delete [] name;
    }

    SafeRelease(&pFontCollection);
    SafeRelease(&pDWriteFactory);
}


```




