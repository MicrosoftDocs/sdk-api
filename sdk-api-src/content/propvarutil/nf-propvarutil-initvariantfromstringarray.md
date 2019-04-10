---
UID: NF:propvarutil.InitVariantFromStringArray
title: InitVariantFromStringArray function (propvarutil.h)
author: windows-sdk-content
description: Initializes a VARIANT structure with an array of strings.
old-location: properties\InitVariantFromStringArray.htm
tech.root: properties
ms.assetid: f46cfc71-9e27-4ba1-8a32-5b279b628732
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitVariantFromStringArray, InitVariantFromStringArray function [Windows Properties], _shell_InitVariantFromStringArray, properties.InitVariantFromStringArray, propvarutil/InitVariantFromStringArray, shell.InitVariantFromStringArray
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2, Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - InitVariantFromStringArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitVariantFromStringArray function


## -description


Initializes a <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure with an array of strings.


## -parameters




### -param prgsz [in]

Type: <b>PCWSTR*</b>

Pointer to an array of strings.


### -param cElems [in]

Type: <b>ULONG</b>

The number of elements in the array pointed to by <i>prgsz</i>.


### -param pvar [out]

Type: <b>VARIANT*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/en-us/library/ms221627(v=VS.85).aspx">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Creates a VT_ARRAY | VT_BSTR variant.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb762336(v=VS.85).aspx">InitVariantFromStringArray</a>.


```cpp
PCWSTR rgStrings[] = {"dog", "cat"};
VARIANT var;

HRESULT hr = InitVariantFromStringArray(rgStrings, ARRAYSIZE(rgStrings), &var);

if (SUCCEEDED(hr))
{
    // var now is valid and has type VT_ARRAY | VT_BSTR.
    VariantClear(&var);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762305(v=VS.85).aspx">InitPropVariantFromString</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762335(v=VS.85).aspx">InitVariantFromString</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776619(v=VS.85).aspx">VariantToStringArray</a>
 

 

