---
UID: NF:propvarutil.PropVariantToInt64Vector
title: PropVariantToInt64Vector function
author: windows-driver-content
description: Extracts data from a PROPVARIANT structure into an Int64 vector.
old-location: properties\PropVariantToInt64Vector.htm
old-project: properties
ms.assetid: cda5589a-726f-4e43-aec4-bb7a7ca62b1a
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: PropVariantToInt64Vector, PropVariantToInt64Vector function [Windows Properties], _shell_PropVariantToInt64Vector, properties.PropVariantToInt64Vector, propvarutil/PropVariantToInt64Vector, shell.PropVariantToInt64Vector
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
req.typenames: PROPVAR_COMPARE_UNIT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PropVariantToInt64Vector
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PropVariantToInt64Vector function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into an <b>Int64</b> vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param prgn [out]

Type: <b>LONGLONG*</b>

Points to a buffer containing <i>crgn</i>   <b>LONGLONG</b> values. When this function returns, the buffer has been initialized with <i>pcElem</i>  <b>LONGLONG</b> elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.


### -param crgn [in]

Type: <b>ULONG</b>

Size of the buffer pointed to by <i>prgn</i> in elements.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>LONGLONG</b> values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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
The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> contained more than <i>crgn</i> values. The buffer pointed to by <i>prgn</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> was not of the appropriate type

</td>
</tr>
</table>
 




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an vector of <b>LONGLONG</b> values with a fixed number of elements.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_I8</b> or <b>VT_ARRAY</b> | <b>VT_I8</b>, this helper function extracts up to <i>crgn</i>   <b>LONGLONG</b> values and places them into the buffer pointed to by <i>prgn</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the prgn buffer, this function returns an error and sets <i>pcElem</i> to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToInt64Vector">PropVariantToInt64Vector</a> to access an Int64 vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
LONGLONG rgLongs[4]; // The application is expecting propvar to hold 4 LONGLONGs in a vector
ULONG cElems;
HRESULT hr = PropVariantToInt64Vector(propvar, rgLongs, ARRAYSIZE(rgLongs), &amp;cElems);
if (SUCCEEDED(hr))
{
     if (cElems == ARRAYSIZE(rgLongs))
     {
         // The application got 4 LONGLONGs which are now stored in rgLongs
     }
     else
     {
         // The application got cElems which are stored in the first cElems elements of rgLongs
     }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromInt64Vector">InitPropVariantFromInt64Vector</a>



<a href="shell.PropVariantGetInt64Elem">PropVariantGetInt64Elem</a>



<a href="shell.PropVariantToInt64">PropVariantToInt64</a>



<a href="shell.PropVariantToInt64VectorAlloc">PropVariantToInt64VectorAlloc</a>



<a href="shell.VariantToInt64Array">VariantToInt64Array</a>
 

 

