---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# PropVariantToFileTimeVector function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a FILETIME vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param prgft [out]

Type: <b>FILETIME*</b>

 Points to a buffer containing <i>crgft</i> FILETIME values. When this function returns, the buffer has been initialized with <i>pcElem</i> FILETIME elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. 


### -param crgft [in]

Type: <b>ULONG</b>

 Size in elements of the buffer pointed to by <i>prgft</i>. 


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of FILETIME elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

Returns one of the following values.

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
The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> contained more than crgn values. The buffer pointed to by <i>prgft</i>.

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



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a filetime vector value with a fixed number of elements.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_VECTOR | VT_FILETIME, this helper function extracts up to <i>crgft</i> FILETIME values and places them into the buffer pointed to by <i>prgft</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the <i>prgft</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.

The output FILETIMEs will use the same time zone as the source FILETIMEs.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToFileTimeVector">PropVariantToFileTimeVector</a> to access a FILETIME vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
FILETIME rgTimes[4]; // The application is expecting propvar to hold 4 FILETIMEs in a vector
ULONG cTimes;
HRESULT hr = PropVariantToFileTimeVector(propvar, rgTime, ARRAYSIZE(rgTime), &amp;cTimes);
if (SUCCEEDED(hr))
{
     if (cTimes == ARRAYSIZE(rgTime))
     {
         // The application got 4 FILETIMEs which are now stored in rgTime
     }
     else
     {
         // The application got cTimes which are stored in the first cTimes elements of rgTime
     }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromFileTimeVector">InitPropVariantFromFileTimeVector</a>



<a href="shell.PropVariantToFileTime">PropVariantToFileTime</a>



<a href="shell.PropVariantToFileTimeVectorAlloc">PropVariantToFileTimeVectorAlloc</a>
 

 

