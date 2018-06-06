---
UID: NF:propvarutil.PropVariantToUInt32VectorAlloc
title: PropVariantToUInt32VectorAlloc function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into a newly-allocated ULONG vector.
old-location: properties\PropVariantToUInt32VectorAlloc.htm
old-project: properties
ms.assetid: 8127b569-aa20-4a15-9da5-cc7c3a7c5243
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToUInt32VectorAlloc, PropVariantToUInt32VectorAlloc function [Windows Properties], _shell_PropVariantToUInt32VectorAlloc, properties.PropVariantToUInt32VectorAlloc, propvarutil/PropVariantToUInt32VectorAlloc, shell.PropVariantToUInt32VectorAlloc
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantToUInt32VectorAlloc
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropVariantToUInt32VectorAlloc function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a newly-allocated <b>ULONG</b> vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pprgn [out]

Type: <b>ULONG**</b>

When this function returns, contains a pointer to a vector of <b>ULONG</b> values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>ULONG</b> values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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
The <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> was not of the appropriate type.

</td>
</tr>
</table>
 




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a vector of <b>ULONG</b> values.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_UI4</b> or <b>VT_ARRAY</b> | <b>VT_UI4</b>, this function extracts a vector of <b>ULONG</b> values into a newly allocated vector. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed. 


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToUInt32VectorAlloc">PropVariantToUInt32VectorAlloc</a> to access a <b>ULONG</b> vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is expecting propvar to contain a vector of ULONG values.
ULONG *prgLongs;
ULONG cElems;
HRESULT hr = PropVariantToUInt32VectorAlloc(propvar, &amp;prgLongs, &amp;cElems);
if (SUCCEEDED(hr))
{
     // prgLongs now points to a vector of cElems ULONG.
     CoTaskMemFree(prgLongs);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromUInt32Vector">InitPropVariantFromUInt32Vector</a>



<a href="shell.PropVariantGetUInt32Elem">PropVariantGetUInt32Elem</a>



<a href="shell.PropVariantToUInt32">PropVariantToUInt32</a>



<a href="shell.PropVariantToUInt32Vector">PropVariantToUInt32Vector</a>



<a href="shell.VariantToUInt32Array">VariantToUInt32Array</a>
 

 

