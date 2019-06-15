---
UID: NF:propvarutil.PropVariantGetUInt32Elem
title: PropVariantGetUInt32Elem function (propvarutil.h)
author: windows-sdk-content
description: Extracts a single unsigned Int32 element from a PROPVARIANT structure of type VT_UI4, VT_VECTOR | VT_UI4, or VT_ARRAY | VT_UI4.
old-location: properties\PropVariantGetUInt32Elem.htm
tech.root: properties
ms.assetid: b31975b6-d717-4e8d-bf5a-2ade96034031
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PropVariantGetUInt32Elem, PropVariantGetUInt32Elem function [Windows Properties], _shell_PropVariantGetUInt32Elem, properties.PropVariantGetUInt32Elem, propvarutil/PropVariantGetUInt32Elem, shell.PropVariantGetUInt32Elem
ms.topic: function
f1_keywords: ["propvarutil/PropVariantGetUInt32Elem"]
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
 - PropVariantGetUInt32Elem
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
---

# PropVariantGetUInt32Elem function


## -description


Extracts a single unsigned Int32 element from a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure of type VT_UI4, VT_VECTOR | VT_UI4, or VT_ARRAY | VT_UI4.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

The source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structure.


### -param iElem [in]

Type: <b>ULONG</b>

A vector or array index; otherwise, <i>iElem</i> must be 0.


### -param pnVal [out]

Type: <b>ULONG*</b>

When this function returns, contains the extracted unsigned Int32 value.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function works for <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> structures of the following types: 

                

<ul>
<li>VT_UI4</li>
<li>VT_VECTOR | VT_UI4</li>
<li>VT_ARRAY | VT_UI4</li>
</ul>
If the source <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a> has type VT_UI4, <i>iElem</i> must be 0. Otherwise, <i>iElem</i> must be less than the number of elements in the vector or array. You can use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelementcount">PropVariantGetElementCount</a> to obtain the number of elements in the vector or array.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetuint32elem">PropVariantGetUInt32Elem</a> with an iteration statement to access the values in a <a href="https://docs.microsoft.com/windows/desktop/api/propidl/ns-propidl-tagpropvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid.

if ((propvar.vt & VT_TYPEMASK) == VT_UI4)
{
    UINT cElem = PropVariantGetElementCount(propvar);
    HRESULT hr = <mark type="const">S_OK</mark>;

    for (UINT iElem = 0; SUCCEEDED(hr) && iElem < cElem; iElem ++)
    {
        ULONG nValue;
        hr = PropVariantGetUInt32Elem(propvar, iElem, &nValue);

        if (SUCCEEDED(hr))
        {
            // nValue is valid now
        }
    }
}
```





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propvarutil/nf-propvarutil-propvariantgetelem">PropVariantGetElem</a>
 

 

