---
UID: NF:propvarutil.InitPropVariantVectorFromPropVariant
title: InitPropVariantVectorFromPropVariant function
author: windows-sdk-content
description: Initializes a vector element in a PROPVARIANT structure with a value stored in another PROPVARIANT.
old-location: properties\InitPropVariantVectorFromPropVariant.htm
tech.root: properties
ms.assetid: 579f80af-38e0-4d3a-9307-5aa5e3fd6770
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: InitPropVariantVectorFromPropVariant, InitPropVariantVectorFromPropVariant function [Windows Properties], properties.InitPropVariantVectorFromPropVariant, propvarutil/InitPropVariantVectorFromPropVariant, shell.InitPropVariantVectorFromPropVariant, shell_InitPropVariantVectorFromPropVariant
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - InitPropVariantVectorFromPropVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# InitPropVariantVectorFromPropVariant function


## -description


Initializes a vector element in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure with a value stored in another <b>PROPVARIANT</b>.


## -parameters




### -param propvarSingle [in]

Type: <b>REFPROPVARIANT</b>

Reference to the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains a single value.


### -param ppropvarVector [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

When this function returns, contains the initialized <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This function is used to convert a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains a single value into a vector value.

For simple source types, this function initializes the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> as a vector of one element.

For a source that contains a string, this function initializes the <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> with zero or more substrings taken from the source string, treating semicolons as delimiters. See <a href="shell.InitPropVariantFromStringAsVector">InitPropVariantFromStringAsVector</a> for more details.

The following input types are supported:
            
                

<ul>
<li>VT_I2</li>
<li>VT_UI2</li>
<li>VT_I4</li>
<li>VT_UI4</li>
<li>VT_I8</li>
<li>VT_UI8</li>
<li>VT_R8</li>
<li>VT_BOOL</li>
<li>VT_DATE</li>
<li>VT_FILETIME</li>
<li>VT_BSTR</li>
<li>VT_LPWSTR</li>
</ul>
Additional types may be supported in the future.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.InitPropVariantVectorFromPropVariant">InitPropVariantVectorFromPropVariant</a>.


```cpp
// PROPVARIANT propvarSource;
// Assume propvarSource is initialized and valid.

if (PropVariantGetElementCount(propvarSource) == 1)
{
    PROPVARIANT propvar;

    HRESULT hr = InitPropVariantVectorFromPropVariant(propvarSource, &propvar);

    if (SUCCEEDED(hr))
    {
       // propvar now is valid and is either VT_EMPTY or contains a vector.
       PropVariantClear(&propvar);
    }
```





## -see-also




<a href="shell.InitPropVariantFromStringAsVector">InitPropVariantFromStringAsVector</a>



<a href="shell.PropVariantGetElem">PropVariantGetElem</a>



<a href="shell.PropVariantGetElementCount">PropVariantGetElementCount</a>
 

 

