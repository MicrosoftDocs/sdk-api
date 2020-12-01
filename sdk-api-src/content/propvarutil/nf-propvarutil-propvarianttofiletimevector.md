---
UID: NF:propvarutil.PropVariantToFileTimeVector
title: PropVariantToFileTimeVector function (propvarutil.h)
description: Extracts data from a PROPVARIANT structure into a FILETIME vector.
helpviewer_keywords: ["PropVariantToFileTimeVector","PropVariantToFileTimeVector function [Windows Properties]","_shell_PropVariantToFileTimeVector","properties.PropVariantToFileTimeVector","propvarutil/PropVariantToFileTimeVector","shell.PropVariantToFileTimeVector"]
old-location: properties\PropVariantToFileTimeVector.htm
tech.root: properties
ms.assetid: ef665f50-3f3b-47db-9133-490305da5341
ms.date: 12/05/2018
ms.keywords: PropVariantToFileTimeVector, PropVariantToFileTimeVector function [Windows Properties], _shell_PropVariantToFileTimeVector, properties.PropVariantToFileTimeVector, propvarutil/PropVariantToFileTimeVector, shell.PropVariantToFileTimeVector
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
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
ms.custom: 19H1
f1_keywords:
 - PropVariantToFileTimeVector
 - propvarutil/PropVariantToFileTimeVector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PropVariantToFileTimeVector
---

# PropVariantToFileTimeVector function


## -description

Extracts data from a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure into a FILETIME vector.

## -parameters

### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param prgft [out]

Type: <b>FILETIME*</b>

 Points to a buffer containing <i>crgft</i> FILETIME values. When this function returns, the buffer has been initialized with <i>pcElem</i> FILETIME elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

### -param crgft [in]

Type: <b>ULONG</b>

 Size in elements of the buffer pointed to by <i>prgft</i>.

### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of FILETIME elements extracted from the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure.

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
The source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> contained more than crgn values. The buffer pointed to by <i>prgft</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> was not of the appropriate type.

</td>
</tr>
</table>

## -remarks

This helper function is used in places where the calling application expects a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> to hold a filetime vector value with a fixed number of elements.

If the source <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> has type VT_VECTOR | VT_FILETIME, this helper function extracts up to <i>crgft</i> FILETIME values and places them into the buffer pointed to by <i>prgft</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the <i>prgft</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.

The output FILETIMEs will use the same time zone as the source FILETIMEs.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletimevector">PropVariantToFileTimeVector</a> to access a FILETIME vector value in a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid
FILETIME rgTimes[4]; // The application is expecting propvar to hold 4 FILETIMEs in a vector
ULONG cTimes;
HRESULT hr = PropVariantToFileTimeVector(propvar, rgTime, ARRAYSIZE(rgTime), &cTimes);
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
}
```

## -see-also

<a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromfiletimevector">InitPropVariantFromFileTimeVector</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletime">PropVariantToFileTime</a>



<a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvarianttofiletimevectoralloc">PropVariantToFileTimeVectorAlloc</a>