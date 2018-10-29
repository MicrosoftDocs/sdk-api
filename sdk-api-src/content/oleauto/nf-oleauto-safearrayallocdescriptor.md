---
UID: NF:oleauto.SafeArrayAllocDescriptor
title: SafeArrayAllocDescriptor function
author: windows-sdk-content
description: Allocates memory for a safe array descriptor.
old-location: automat\safearrayallocdescriptor.htm
tech.root: automat
ms.assetid: 8fe5c802-cdc0-4e7a-9410-ba65f9a5140e
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: SafeArrayAllocDescriptor, SafeArrayAllocDescriptor function [Automation], _oa96_SafeArrayAllocDescriptor, automat.safearrayallocdescriptor, oleauto/SafeArrayAllocDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
api_name:
 - SafeArrayAllocDescriptor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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



This function allows the creation of safe arrays that contain elements with data types other than those provided by <a href="https://msdn.microsoft.com/en-us/library/ms221234(v=VS.85).aspx">SafeArrayCreate</a>. After creating an array descriptor using <b>SafeArrayAllocDescriptor</b>, set the element size in the array descriptor, an call <a href="https://msdn.microsoft.com/en-us/library/ms221468(v=VS.85).aspx">SafeArrayAllocData</a> to allocate memory for the array elements.


#### Examples

The following example creates a safe array using the <b>SafeArrayAllocDescriptor</b> and <a href="https://msdn.microsoft.com/a1f984cd-9638-415d-8582-25b1bdfbd694">SafeArrayAllocData</a> functions.


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




<a href="https://msdn.microsoft.com/a1f984cd-9638-415d-8582-25b1bdfbd694">SafeArrayAllocData</a>



<a href="https://msdn.microsoft.com/aa9c62ba-79b5-4fcf-b3ed-664016486dfc">SafeArrayDestroyData</a>



<a href="https://msdn.microsoft.com/f1e8de45-673b-4f20-a639-18c724c82df1">SafeArrayDestroyDescriptor</a>
 

 

