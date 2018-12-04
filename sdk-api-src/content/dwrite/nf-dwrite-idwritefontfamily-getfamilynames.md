---
UID: NF:dwrite.IDWriteFontFamily.GetFamilyNames
title: IDWriteFontFamily::GetFamilyNames
author: windows-sdk-content
description: Creates a localized strings object that contains the family names for the font family, indexed by locale name.
old-location: directwrite\IDWriteFontFamily_GetFamilyNames.htm
tech.root: DirectWrite
ms.assetid: 89b36a28-c8c7-42aa-89a6-7d8f5ddae3fa
ms.author: windowssdkdev
ms.date: 11/30/2018
ms.keywords: GetFamilyNames, GetFamilyNames method [Direct Write], GetFamilyNames method [Direct Write],IDWriteFontFamily interface, IDWriteFontFamily interface [Direct Write],GetFamilyNames method, IDWriteFontFamily.GetFamilyNames, IDWriteFontFamily::GetFamilyNames, directwrite.IDWriteFontFamily_GetFamilyNames, dwrite/IDWriteFontFamily::GetFamilyNames
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IDWriteFontFamily.GetFamilyNames
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteFontFamily::GetFamilyNames


## -description


 Creates a localized strings object that contains the family names for the font family, indexed by locale name.


## -parameters




### -param names [out]

Type: <b><a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>**</b>

The address of a pointer to the newly created <a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The following code example shows how to get the font family name from a <a href="https://msdn.microsoft.com/1fce3d62-af4e-4d2b-a3fd-e534b5fcdb13">IDWriteFontFamily</a> object.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IDWriteLocalizedStrings* pFamilyNames = NULL;

// Get a list of localized strings for the family name.
if (SUCCEEDED(hr))
{
    hr = pFontFamily-&gt;GetFamilyNames(&amp;pFamilyNames);
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
        hr = pFamilyNames-&gt;FindLocaleName(localeName, &amp;index, &amp;exists);
    }
    if (SUCCEEDED(hr) &amp;&amp; !exists) // if the above find did not find a match, retry with US English
    {
        hr = pFamilyNames-&gt;FindLocaleName(L"en-us", &amp;index, &amp;exists);
    }
}

// If the specified locale doesn't exist, select the first on the list.
if (!exists)
    index = 0;

UINT32 length = 0;

// Get the string length.
if (SUCCEEDED(hr))
{
    hr = pFamilyNames-&gt;GetStringLength(index, &amp;length);
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
    hr = pFamilyNames-&gt;GetString(index, name, length+1);
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/1fce3d62-af4e-4d2b-a3fd-e534b5fcdb13">IDWriteFontFamily</a>
 

 

