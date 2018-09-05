---
UID: NF:dwrite.IDWriteLocalizedStrings.GetStringLength
title: IDWriteLocalizedStrings::GetStringLength
author: windows-sdk-content
description: Gets the length in characters (not including the null terminator) of the string with the specified index.
old-location: directwrite\IDWriteLocalizedStrings_GetStringLength.htm
old-project: DirectWrite
ms.assetid: 8dd55a10-d654-4d09-b2ee-d51e504d83c9
ms.author: windowssdkdev
ms.date: 08/24/2018
ms.keywords: GetStringLength, GetStringLength method [Direct Write], GetStringLength method [Direct Write],IDWriteLocalizedStrings interface, IDWriteLocalizedStrings interface [Direct Write],GetStringLength method, IDWriteLocalizedStrings.GetStringLength, IDWriteLocalizedStrings::GetStringLength, directwrite.IDWriteLocalizedStrings_GetStringLength, dwrite/IDWriteLocalizedStrings::GetStringLength
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dwrite.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>UINT32 length = 0;

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




<a href="https://msdn.microsoft.com/37bfc613-4128-45aa-b6b2-6163d44378e4">IDWriteLocalizedStrings</a>
 

 

