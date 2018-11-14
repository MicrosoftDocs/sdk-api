---
UID: NF:dwrite.IDWriteLocalizedStrings.FindLocaleName
title: IDWriteLocalizedStrings::FindLocaleName
author: windows-sdk-content
description: Gets the zero-based index of the locale name/string pair with the specified locale name.
old-location: directwrite\IDWriteLocalizedStrings_FindLocaleName.htm
tech.root: DirectWrite
ms.assetid: d80032b2-304e-4c48-a7c7-fcda4305cca4
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: FindLocaleName, FindLocaleName method [Direct Write], FindLocaleName method [Direct Write],IDWriteLocalizedStrings interface, IDWriteLocalizedStrings interface [Direct Write],FindLocaleName method, IDWriteLocalizedStrings.FindLocaleName, IDWriteLocalizedStrings::FindLocaleName, directwrite.IDWriteLocalizedStrings_FindLocaleName, dwrite/IDWriteLocalizedStrings::FindLocaleName
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
 - IDWriteLocalizedStrings.FindLocaleName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- dwrite.h
: 
- IDWriteLocalizedStrings.FindLocaleName
: 
---

# IDWriteLocalizedStrings::FindLocaleName


## -description


 Gets the zero-based index of the locale name/string pair with the specified locale name.


## -parameters




### -param localeName [in]

Type: <b>const WCHAR*</b>

A null-terminated array of characters containing the locale name to look for.


### -param index [out]

Type: <b>UINT32*</b>

The zero-based index of the locale name/string pair. This method initializes <i>index</i> to <b>UINT_MAX</b>.


### -param exists [out]

Type: <b>BOOL*</b>

When this method returns, contains <b>TRUE</b> if the locale name exists; otherwise, <b>FALSE</b>. This method initializes <i>exists</i> to <b>FALSE</b>.


## -returns



Type: <b>HRESULT</b>

If the specified locale name does not exist, the return value is <b>S_OK</b>, 
     but <i>index</i> is <b>UINT_MAX</b> and <i>exists</i> is <b>FALSE</b>.





## -remarks



Note that if the locale name does not exist, the return value is a success and the <i>exists</i> parameter is <b>FALSE</b>. If you are getting the font family name for a font and the specified locale name does not exist, one option is to set the index to 0 as shown below.  There is always at least one locale for a font family.


```cpp
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

```





## -see-also




<a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>
 

 

