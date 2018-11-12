---
UID: NN:dwrite.IDWriteLocalizedStrings
title: IDWriteLocalizedStrings
author: windows-sdk-content
description: Represents a collection of strings indexed by locale name.
old-location: directwrite\IDWriteLocalizedStrings.htm
tech.root: DirectWrite
ms.assetid: 37bfc613-4128-45aa-b6b2-6163d44378e4
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: IDWriteLocalizedStrings, IDWriteLocalizedStrings interface [Direct Write], IDWriteLocalizedStrings interface [Direct Write],described, directwrite.IDWriteLocalizedStrings, dwrite/IDWriteLocalizedStrings
ms.prod: windows
ms.technology: windows-sdk
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
 - IDWriteLocalizedStrings
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteLocalizedStrings interface


## -description


 Represents a collection of strings indexed by locale name.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteLocalizedStrings</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDWriteLocalizedStrings</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteLocalizedStrings</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d80032b2-304e-4c48-a7c7-fcda4305cca4">FindLocaleName</a>
</td>
<td align="left" width="63%">
 Gets the zero-based index of the locale name/string pair with the specified locale name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5aafda50-327d-4fee-9c2b-fb3f23482c60">GetCount</a>
</td>
<td align="left" width="63%">
 Gets the number of language/string pairs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9256845d-c75e-4def-8466-f3b796f74817">GetLocaleName</a>
</td>
<td align="left" width="63%">
 Copies the locale name with the specified index to the specified array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a175380b-1109-476d-8bd7-9ba0753c125f">GetLocaleNameLength</a>
</td>
<td align="left" width="63%">
 Gets the length in characters (not including the null terminator) of the locale name with the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/adb7358b-044b-440b-8429-be715d22cd83">GetString</a>
</td>
<td align="left" width="63%">
 Copies the string with the specified index to the specified array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8dd55a10-d654-4d09-b2ee-d51e504d83c9">GetStringLength</a>
</td>
<td align="left" width="63%">
 Gets the length in characters (not including the null terminator) of the string with the specified index.

</td>
</tr>
</table> 


## -remarks



The set of strings represented by an <b>IDWriteLocalizedStrings</b> are indexed by a zero based <i>UINT32</i> number that maps to a locale.  The numeric index for a specific locale is retreived by using the <a href="https://msdn.microsoft.com/d80032b2-304e-4c48-a7c7-fcda4305cca4">FindLocaleName</a> method.

A common use for the <b>IDWriteLocalizedStrings</b> interface is to hold a list of localized font family names created by using the <a href="https://msdn.microsoft.com/89b36a28-c8c7-42aa-89a6-7d8f5ddae3fa">IDWriteFontFamily::GetFamilyNames</a> method.  The following example shows how to get the family name for the "en-us" locale.


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




