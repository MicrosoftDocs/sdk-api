---
UID: NF:oleauto.SafeArrayAllocDescriptor
title: SafeArrayAllocDescriptor function (oleauto.h)
description: Allocates memory for a safe array descriptor.
helpviewer_keywords: ["SafeArrayAllocDescriptor","SafeArrayAllocDescriptor function [Automation]","_oa96_SafeArrayAllocDescriptor","automat.safearrayallocdescriptor","oleauto/SafeArrayAllocDescriptor"]
old-location: automat\safearrayallocdescriptor.htm
tech.root: automat
ms.assetid: 8fe5c802-cdc0-4e7a-9410-ba65f9a5140e
ms.date: 12/05/2018
ms.keywords: SafeArrayAllocDescriptor, SafeArrayAllocDescriptor function [Automation], _oa96_SafeArrayAllocDescriptor, automat.safearrayallocdescriptor, oleauto/SafeArrayAllocDescriptor
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SafeArrayAllocDescriptor
 - oleauto/SafeArrayAllocDescriptor
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayAllocDescriptor
---

# SafeArrayAllocDescriptor function


## -description

Allocates memory for a safe array descriptor.

## -parameters

### -param cDims [in]

The number of dimensions of the array.

### -param ppsaOut [out]

The safe array descriptor.

## -returns

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The argument <i>psa</i> was not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The array could not be locked.

</td>
</tr>
</table>

## -remarks

This function allows the creation of safe arrays that contain elements with data types other than those provided by <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraycreate">SafeArrayCreate</a>. After creating an array descriptor using <b>SafeArrayAllocDescriptor</b>, set the element size in the array descriptor, a call <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayallocdata">SafeArrayAllocData</a> to allocate memory for the array elements.


#### Examples

The following example creates a safe array using the <b>SafeArrayAllocDescriptor</b> and <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayallocdata">SafeArrayAllocData</a> functions.


```cpp
SAFEARRAY *psa;
unsigned int ndim =  2;
HRESULT hresult = SafeArrayAllocDescriptor( ndim, &psa );
if( FAILED( hresult ) )
   return ERR_OutOfMemory;
(psa)->rgsabound[ 0 ].lLbound = 0;
(psa)->rgsabound[ 0 ].cElements = 5;
(psa)->rgsabound[ 1 ].lLbound = 1;
(psa)->rgsabound[ 1 ].cElements = 4;
hresult = SafeArrayAllocData( psa );
if( FAILED( hresult ) ) {
   SafeArrayDestroyDescriptor( psa )
   return ERR_OutOfMemory;
}
```

## -see-also

<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearrayallocdata">SafeArrayAllocData</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraydestroydata">SafeArrayDestroyData</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-safearraydestroydescriptor">SafeArrayDestroyDescriptor</a>