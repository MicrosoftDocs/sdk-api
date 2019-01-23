---
UID: NF:propvarutil.PropVariantToStringVector
title: PropVariantToStringVector function
author: windows-sdk-content
description: Extracts a vector of strings from a PROPVARIANT structure.
old-location: properties\PropVariantToStringVector.htm
tech.root: properties
ms.assetid: 6618ee02-1939-4c9c-8690-a8cd5d668cdb
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PropVariantToStringVector, PropVariantToStringVector function [Windows Properties], _shell_PropVariantToStringVector, properties.PropVariantToStringVector, propvarutil/PropVariantToStringVector, shell.PropVariantToStringVector
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
 - PropVariantToStringVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToStringVector function


## -description


Extracts a vector of strings from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param prgsz [out]

Type: <b>PWSTR*</b>

Pointer to a vector of string pointers. When this function returns, the buffer has been initialized with <i>pcElem</i> elements pointing to newly allocated strings containing the data extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.


### -param crgsz [in]

Type: <b>ULONG</b>

Size of the buffer pointed to by <i>prgsz</i>, in elements.


### -param pcElem [out]

Type: <b>ULONG*</b>

 When this function returns, contains the count of strings extracted from source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Returns <b>S_OK</b> if successful, or an error value otherwise.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The source<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>contained more than <i>crgsz</i> values. The buffer pointed to by <i>prgsz</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>was not of the appropriate type.

</td>
</tr>
</table>
 




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an vector of string values with a fixed number of elements.

This function works for the following <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> types:
            

<ul>
<li>VT_VECTOR | VT_LPWSTR</li>
<li>VT_VECTOR | VT_BSTR</li>
<li>VT_ARRAY | VT_BSTR</li>
</ul>
If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has a supported type, this helper function extracts up to <i>crgsz</i> string values and places an allocated copy of each into the buffer pointed to by prgsz. If the<b>PROPVARIANT</b>contains more elements than will fit into the <i>prgsz</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.

Since each string in pointed to by the output buffer has been newly allocated, the calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to free each string in the output buffer when they are no longer needed.

If a <b>BSTR</b> in the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> is <b>NULL</b>, it is converted to a newly allocated string containing "" in the output.


#### Examples


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
LPWSTR rgszStrings; // The application is expecting propvar to hold 4 strings in a vector
ULONG cElems;
HRESULT hr = PropVariantToStringVector(propvar, rgszStrings, ARRAYSIZE(rgszStrings), &cElems);
if (SUCCEEDED(hr))
{
     if (cElems == ARRAYSIZE(rgszStrings))
     {
         // The application got 4 string which are now stored in rgszStrings
     }
     else
     {
         // The application got cElems which are stored in the first cElems elements of rgLongs
     }
 
    // Free the cElems strings that PropVariantToStringVector allocated
    for (ULONG i = 0; i < cElems; i++)
    {
        CoTaskMemFree(rgszStrings[i]);
    }
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762307(v=VS.85).aspx">InitPropVariantFromStringVector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776527(v=VS.85).aspx">PropVariantGetStringElem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776559(v=VS.85).aspx">PropVariantToString</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776562(v=VS.85).aspx">PropVariantToStringVectorAlloc</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776619(v=VS.85).aspx">VariantToStringArray</a>
 

 

