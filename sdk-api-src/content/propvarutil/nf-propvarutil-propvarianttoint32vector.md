---
UID: NF:propvarutil.PropVariantToInt32Vector
title: PropVariantToInt32Vector function
author: windows-sdk-content
description: Extracts a vector of long values from a PROPVARIANT structure.
old-location: properties\PropVariantToInt32Vector.htm
old-project: properties
ms.assetid: 771fa1d7-c648-49d4-a6a2-5aa23f8c20b7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PropVariantToInt32Vector, PropVariantToInt32Vector function [Windows Properties], _shell_PropVariantToInt32Vector, properties.PropVariantToInt32Vector, propvarutil/PropVariantToInt32Vector, shell.PropVariantToInt32Vector
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propvarutil.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
 - PropVariantToInt32Vector
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PropVariantToInt32Vector function


## -description


Extracts a vector of <b>long</b> values from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param prgn [out]

Type: <b>LONG*</b>

Points to a buffer containing <i>crgn</i>   <b>LONG</b> values. When this function returns, the buffer has been initialized with <i>pcElem</i>   <b>LONG</b> elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.


### -param crgn [in]

Type: <b>ULONG</b>

Size of the buffer pointed to by <i>prgn</i> in elements.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>LONG</b> elements extracted from source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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
The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> contained more than crgn values. The buffer pointed to by <i>prgn</i>.

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



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an vector of <b>LONG</b> values with a fixed number of elements.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_I4</b> or <b>VT_ARRAY</b> | <b>VT_I4</b>, this helper function extracts up to <i>crgn</i>   <b>LONG</b> values and places them into the buffer pointed to by <i>prgn</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the <i>prgn</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776551(v=VS.85).aspx">PropVariantToInt32Vector</a> to access an Int32 vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
LONG rgLongs[4]; // The application is expecting propvar to hold 4 LONGs in a vector
ULONG cElems;
HRESULT hr = PropVariantToInt32Vector(propvar, rgLongs, ARRAYSIZE(rgLongs), &amp;cElems);
if (SUCCEEDED(hr))
{
     if (cElems == ARRAYSIZE(rgLongs))
     {
         // The application got 4 LONGs which are now stored in rgLongs
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




<a href="https://msdn.microsoft.com/en-us/library/Bb762300(v=VS.85).aspx">InitPropVariantFromInt32Vector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776525(v=VS.85).aspx">PropVariantGetInt32Elem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776550(v=VS.85).aspx">PropVariantToInt32</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776552(v=VS.85).aspx">PropVariantToInt32VectorAlloc</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776609(v=VS.85).aspx">VariantToInt32Array</a>
 

 

