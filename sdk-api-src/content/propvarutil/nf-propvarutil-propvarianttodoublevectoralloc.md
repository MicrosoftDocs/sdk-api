---
UID: NF:propvarutil.PropVariantToDoubleVectorAlloc
title: PropVariantToDoubleVectorAlloc function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into a newly-allocated double vector.
old-location: properties\PropVariantToDoubleVectorAlloc.htm
tech.root: properties
ms.assetid: 80f05530-a92b-4877-80fa-efac8e999510
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: PropVariantToDoubleVectorAlloc, PropVariantToDoubleVectorAlloc function [Windows Properties], _shell_PropVariantToDoubleVectorAlloc, properties.PropVariantToDoubleVectorAlloc, propvarutil/PropVariantToDoubleVectorAlloc, shell.PropVariantToDoubleVectorAlloc
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
 - PropVariantToDoubleVectorAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToDoubleVectorAlloc function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a newly-allocated double vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pprgn [out]

Type: <b>DOUBLE**</b>

When this function returns, contains a pointer to a vector of double values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of double elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a double vector value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_VECTOR | VT_R8 or VT_ARRAY | VT_R8, this function extracts a vector of double values into a newly allocated vector of DOUBLE values. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the vector pointed to by <i>pprgn</i> when it is no longer needed.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.PropVariantToDoubleVector">PropVariantToDoubleVector</a> to access a double vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// IPropertyStore *ppropstore;
// Assume variable ppropstore is initialized and valid
PROPVARIANT propvar = {0};
HRESULT hr = ppropstore-&gt;GetValue(PKEY_GPS_DestLongitude, &amp;propvar);
if (SUCCEEDED(hr))
{
     // PKEY_GPS_DestLongitude is expected to produce a VT_VECTOR | VT_R8 with three values, or VT_EMPTY
     // PropVariantToDoubleVectorAlloc will return an error for VT_EMPTY
     DOUBLE *rgLongitude;
     ULONG cElem;
     hr = PropVariantToDoubleVectorAlloc(propvar, &amp;rgLongitude, &amp;cElem);
     if (SUCCEEDED(hr))
     {
         if (cElem == 3)
         {
              // rgLongitude contains 3 doubles representing the degrees, minutes, and seconds of longitude
         }
         CoTaskMemFree(rgLongitude);
     }
     else
     {
          // propvar either is VT_EMPTY, or contains something other than a vector of  doubles
     }
     PropVariantClear(&amp;propvar);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitPropVariantFromDoubleVector">InitPropVariantFromDoubleVector</a>



<a href="shell.PropVariantGetDoubleElem">PropVariantGetDoubleElem</a>



<a href="shell.PropVariantToDouble">PropVariantToDouble</a>



<a href="shell.PropVariantToDoubleVector">PropVariantToDoubleVector</a>



<a href="shell.VariantToDoubleArray">VariantToDoubleArray</a>
 

 

