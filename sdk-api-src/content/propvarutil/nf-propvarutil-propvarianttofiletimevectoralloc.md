---
UID: NF:propvarutil.PropVariantToFileTimeVectorAlloc
title: PropVariantToFileTimeVectorAlloc function
author: windows-sdk-content
description: Extracts data from a PROPVARIANT structure into a newly-allocated FILETIME vector.
old-location: properties\PropVariantToFileTimeVectorAlloc.htm
tech.root: properties
ms.assetid: 2d0125fe-f4af-451b-8dc7-d29a35cc927e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: PropVariantToFileTimeVectorAlloc, PropVariantToFileTimeVectorAlloc function [Windows Properties], _shell_PropVariantToFileTimeVectorAlloc, properties.PropVariantToFileTimeVectorAlloc, propvarutil/PropVariantToFileTimeVectorAlloc, shell.PropVariantToFileTimeVectorAlloc
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
 - PropVariantToFileTimeVectorAlloc
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
- apiref
: 
- 
: 
- PropVariantToFileTimeVectorAlloc
: 
---

# PropVariantToFileTimeVectorAlloc function


## -description


Extracts data from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure into a newly-allocated FILETIME vector.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pprgft [out]

Type: <b>FILETIME**</b>

 When this function returns, contains a pointer to a vector of FILETIME values extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of FILETIME elements extracted from source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The<a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>was not of the appropriate type.

</td>
</tr>
</table>
 




## -remarks



This helper function is used in places where the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a FILETIME vector value.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_VECTOR | VT_FILETIME, this function extracts a vector of FILETIMEs values into a newly allocated vector of FILETIME values. The calling application is responsible for using <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> to release the vector pointed to by <i>pprgft</i> when it is no longer needed.

The output FILETIMEs will use the same time zone as the source FILETIMEs.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776544(v=VS.85).aspx">PropVariantToFileTimeVectorAlloc</a> to access a FILETIME vector value in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid. 
// The application is expecting propvar to contain a vector of FILETIME values.
BOOL *prgTimes;
ULONG cTimes;
HRESULT hr = PropVariantToBooleanVectorAlloc(propvar, &amp;prgTimes, &amp;cTimes);
if (SUCCEEDED(hr))
{
     // prgTimes now points to a vector of cTimes file times.
     CoTaskMemFree(prgTimes);
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb762294(v=VS.85).aspx">InitPropVariantFromFileTimeVector</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776542(v=VS.85).aspx">PropVariantToFileTime</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776543(v=VS.85).aspx">PropVariantToFileTimeVector</a>
 

 

