---
UID: NF:dwrite.IDWriteLocalizedStrings.GetStringLength
title: IDWriteLocalizedStrings::GetStringLength
author: windows-sdk-content
description: Gets the length in characters (not including the null terminator) of the string with the specified index.
old-location: directwrite\IDWriteLocalizedStrings_GetStringLength.htm
tech.root: DirectWrite
ms.assetid: 8dd55a10-d654-4d09-b2ee-d51e504d83c9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetStringLength, GetStringLength method [Direct Write], GetStringLength method [Direct Write],IDWriteLocalizedStrings interface, IDWriteLocalizedStrings interface [Direct Write],GetStringLength method, IDWriteLocalizedStrings.GetStringLength, IDWriteLocalizedStrings::GetStringLength, directwrite.IDWriteLocalizedStrings_GetStringLength, dwrite/IDWriteLocalizedStrings::GetStringLength
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
 - IDWriteLocalizedStrings.GetStringLength
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteLocalizedStrings::GetStringLength


## -description


 Gets the length in characters (not including the null terminator) of the string with the specified index.


## -parameters




### -param index

Type: <b>UINT32</b>

A zero-based index of the language/string pair.


### -param length [out]

Type: <b>UINT32*</b>

The length in characters of the string, not including the null terminator, from the language/string pair.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use <b>GetStringLength</b> to get the string length before calling the <a href="https://msdn.microsoft.com/adb7358b-044b-440b-8429-be715d22cd83">IDWriteLocalizedStrings::GetString</a> method, as shown in the following code.


```cpp
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




<a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>
 

 

