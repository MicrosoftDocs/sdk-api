---
UID: NF:propvarutil.PropVariantToBooleanVectorAlloc
title: PropVariantToBooleanVectorAlloc function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into a newly allocated Boolean vector.
old-location: properties\PropVariantToBooleanVectorAlloc.htm
old-project: properties
ms.assetid: 241f43b6-5ff0-4ce6-b0a4-59dc9cb6cf8f
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PropVariantToBooleanVectorAlloc, PropVariantToBooleanVectorAlloc function [Windows Properties], _shell_PropVariantToBooleanVectorAlloc, properties.PropVariantToBooleanVectorAlloc, propvarutil/PropVariantToBooleanVectorAlloc, shell.PropVariantToBooleanVectorAlloc
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PropVariantToBooleanVectorAlloc
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PropVariantToBooleanVectorAlloc function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a newly allocated Boolean vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pprgf [out]

Type: <b>BOOL**</b>

When this function returns, contains a pointer to a vector of Boolean values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of Boolean elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a Boolean vector value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_VECTOR | VT_BOOL or VT_ARRAY | VT_BOOL, this function extracts a vector of Boolean values into a newly allocated vector of <b>BOOL</b> values. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the vector pointed to by <i>pprgf</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToBooleanVectorAlloc">PropVariantToBooleanVectorAlloc</a> to access a Boolean vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. The application is 
// expecting propvar to contain a vector of Boolean values.
BOOL *prgFlags;
ULONG cFlags;
HRESULT hr = PropVariantToBooleanVectorAlloc(propvar, &amp;prgFlags, &amp;cFlags);

if (SUCCEEDED(hr))
{
     // The prgFlags variable now points to a vector that contains a count
     // of cFlags flags.
     CoTaskMemFree(prgFlags);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromBooleanVector">InitPropVariantFromBooleanVector</a>



<a href="shell.IsPropVariantVector">IsPropVariantVector</a>



<a href="shell.PropVariantGetBooleanElem">PropVariantGetBooleanElem</a>



<a href="shell.PropVariantToBooleanVector">PropVariantToBooleanVector</a>
 

 

