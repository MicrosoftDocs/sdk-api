---
UID: NF:propvarutil.PropVariantToUInt16Vector
title: PropVariantToUInt16Vector function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into an unsigned short vector.
old-location: properties\PropVariantToUInt16Vector.htm
tech.root: properties
ms.assetid: 34fe404c-cef6-47d9-9eaf-8ab151bd4726
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: PropVariantToUInt16Vector, PropVariantToUInt16Vector function [Windows Properties], _shell_PropVariantToUInt16Vector, properties.PropVariantToUInt16Vector, propvarutil/PropVariantToUInt16Vector, shell.PropVariantToUInt16Vector
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
 - PropVariantToUInt16Vector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToUInt16Vector function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into an <b>unsigned short</b> vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param prgn [out]

Type: <b>USHORT*</b>

Points to a buffer containing <i>crgn</i> <b>unsigned short</b> values. When this function returns, the buffer has been initialized with <i>pcElem</i> <b>unsigned short</b> elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>. 


### -param crgn [in]

Type: <b>ULONG</b>

Size of the buffer pointed to by <i>prgn</i> in elements.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of <b>unsigned short</b> values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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
The <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> was not of the appropriate type.

</td>
</tr>
</table>
 




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold an vector of <b>unsigned short</b> values with a fixed number of elements.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type <b>VT_VECTOR</b> | <b>VT_UI2</b> or <b>VT_ARRAY</b> | <b>VT_UI2</b>, this helper function extracts up to <i>crgn</i>   <b>unsigned short</b> values and places them into the buffer pointed to by <i>prgn</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the prgn buffer, this function returns an error and sets <i>pcElem</i> to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776566(v=VS.85).aspx">PropVariantToUInt16Vector</a> to access an <b>unsigned short</b> vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
USHORT rgShorts[4]; // The application is expecting propvar to hold 4 USHORTs in a vector
ULONG cElems;
HRESULT hr = PropVariantToUInt16Vector(propvar, rgShorts, ARRAYSIZE(rgShorts), &amp;cElems);
if (SUCCEEDED(hr))
{
     if (cElems == ARRAYSIZE(rgShorts))
     {
         // The application got 4 USHORTs which are now stored in rgShorts
     }
     else
     {
         // The application got cElems which are stored in the first cElems elements of rgShorts
     }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762310(v=VS.85).aspx">InitPropVariantFromUInt16Vector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776528(v=VS.85).aspx">PropVariantGetUInt16Elem</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776565(v=VS.85).aspx">PropVariantToUInt16</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776567(v=VS.85).aspx">PropVariantToUInt16VectorAlloc</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776624(v=VS.85).aspx">VariantToUInt16Array</a>
 

 

