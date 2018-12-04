---
UID: NF:propvarutil.PropVariantToInt16VectorAlloc
title: PropVariantToInt16VectorAlloc function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into a newly allocated Int16 vector.
old-location: properties\PropVariantToInt16VectorAlloc.htm
tech.root: properties
ms.assetid: 489aff33-2faa-480a-a146-67f6ef4b8b93
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: PropVariantToInt16VectorAlloc, PropVariantToInt16VectorAlloc function [Windows Properties], _shell_PropVariantToInt16VectorAlloc, properties.PropVariantToInt16VectorAlloc, propvarutil/PropVariantToInt16VectorAlloc, shell.PropVariantToInt16VectorAlloc
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
 - PropVariantToInt16VectorAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToInt16VectorAlloc function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a newly allocated <b>Int16</b> vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pprgn [out]

Type: <b>SHORT**</b>

When this function returns, contains a pointer to a vector of <b>Int16</b> values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

 When this function returns, contains the count of <b>Int16</b> elements extracted from source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an <b>Int16</b> vector value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_VECTOR | VT_I2 or VT_ARRAY | VT_I2, this function extracts a vector of <b>Int16</b> values into a newly allocated vector of SHORT values. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed.


#### Examples

This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an Int16 vector value.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is expecting propvar to contain a vector of Int16 values.
SHORT *prgShorts;
ULONG cElems;
HRESULT hr = PropVariantToBooleanVectorAlloc(propvar, &amp; prgShorts, &amp;cElems);
if (SUCCEEDED(hr))
{
     // prgShorts now points to a vector of cElems SHORTs.
     CoTaskMemFree(prgShorts);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromInt16Vector">InitPropVariantFromInt16Vector</a>



<a href="shell.PropVariantGetInt16Elem">PropVariantGetInt16Elem</a>



<a href="shell.PropVariantToInt16">PropVariantToInt16</a>



<a href="shell.PropVariantToInt16Vector">PropVariantToInt16Vector</a>



<a href="shell.VariantToInt16Array">VariantToInt16Array</a>
 

 

