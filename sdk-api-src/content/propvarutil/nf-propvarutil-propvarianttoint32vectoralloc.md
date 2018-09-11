---
UID: NF:propvarutil.PropVariantToInt32VectorAlloc
title: PropVariantToInt32VectorAlloc function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into a newly-allocated Int32 vector.
old-location: properties\PropVariantToInt32VectorAlloc.htm
tech.root: properties
ms.assetid: db46f266-9ce0-468a-be35-4a7254e9a769
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropVariantToInt32VectorAlloc, PropVariantToInt32VectorAlloc function [Windows Properties], _shell_PropVariantToInt32VectorAlloc, properties.PropVariantToInt32VectorAlloc, propvarutil/PropVariantToInt32VectorAlloc, shell.PropVariantToInt32VectorAlloc
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
 - PropVariantToInt32VectorAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToInt32VectorAlloc function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a newly-allocated <b>Int32</b> vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pprgn [out]

Type: <b>LONG**</b>

When this function returns, contains a pointer to a vector of <b>LONG</b> values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. 


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>LONG</b> elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>was not of the appropriate type.

</td>
</tr>
</table>
 




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an Int32 vector value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_I4</b> or <b>VT_ARRAY</b> | <b>VT_I4</b>, this function extracts a vector of <b>LONG</b> values into a newly allocated vector. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed. 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776552(v=VS.85).aspx">PropVariantToInt32VectorAlloc</a> to access an <b>LONG</b> vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is expecting propvar to contain a vector of LONG values.
LONG *prgLongs;
ULONG cElems;
HRESULT hr = PropVariantToInt32VectorAlloc(propvar, &prgLongs, &cElems);
if (SUCCEEDED(hr))
{
     // prgLongs now points to a vector of cElems LONGs.
     CoTaskMemFree(prgLongs);
}
```





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762300(v=VS.85).aspx">InitPropVariantFromInt32Vector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776525(v=VS.85).aspx">PropVariantGetInt32Elem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776550(v=VS.85).aspx">PropVariantToInt32</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776551(v=VS.85).aspx">PropVariantToInt32Vector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776609(v=VS.85).aspx">VariantToInt32Array</a>
 

 

