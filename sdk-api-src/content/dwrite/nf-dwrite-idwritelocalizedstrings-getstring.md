---
UID: NF:dwrite.IDWriteLocalizedStrings.GetString
title: IDWriteLocalizedStrings::GetString
author: windows-sdk-content
description: Copies the string with the specified index to the specified array.
old-location: directwrite\IDWriteLocalizedStrings_GetString.htm
tech.root: DirectWrite
ms.assetid: adb7358b-044b-440b-8429-be715d22cd83
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetString, GetString method [Direct Write], GetString method [Direct Write],IDWriteLocalizedStrings interface, IDWriteLocalizedStrings interface [Direct Write],GetString method, IDWriteLocalizedStrings.GetString, IDWriteLocalizedStrings::GetString, directwrite.IDWriteLocalizedStrings_GetString, dwrite/IDWriteLocalizedStrings::GetString
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
 - IDWriteLocalizedStrings.GetString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDWriteLocalizedStrings::GetString


## -description


 Copies the string with the specified index to the specified array.


## -parameters




### -param index

Type: <b>UINT32</b>

The zero-based index of the language/string pair to be examined.


### -param stringBuffer [out]

Type: <b>WCHAR*</b>

The null terminated array of characters that receives the string from the language/string pair.  The buffer allocated for this array should be at least the size of <i>size</i>. <a href="https://msdn.microsoft.com/8dd55a10-d654-4d09-b2ee-d51e504d83c9">GetStringLength</a> can be used to get the size of the array before using this method.


### -param size

Type: <b>UINT32</b>

The size of the array in characters. The size must include space for the terminating
     null character. <a href="https://msdn.microsoft.com/8dd55a10-d654-4d09-b2ee-d51e504d83c9">GetStringLength</a> can be used to get the size of the array before using this method.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The string returned must be allocated by the caller.  You can get the size of the string by using the <a href="https://msdn.microsoft.com/8dd55a10-d654-4d09-b2ee-d51e504d83c9">GetStringLength</a> method prior to calling <b>GetString</b>, as shown in the following example.


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
 

 

