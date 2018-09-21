---
UID: NF:propvarutil.PropVariantToBooleanVector
title: PropVariantToBooleanVector function
author: windows-sdk-content
description: Extracts a Boolean vector from a PROPVARIANT structure.
old-location: properties\PropVariantToBooleanVector.htm
tech.root: properties
ms.assetid: 93ccd129-4fa4-40f3-96f3-b87b50414b0a
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: PropVariantToBooleanVector, PropVariantToBooleanVector function [Windows Properties], _shell_PropVariantToBooleanVector, properties.PropVariantToBooleanVector, propvarutil/PropVariantToBooleanVector, shell.PropVariantToBooleanVector
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
 - PropVariantToBooleanVector
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# PropVariantToBooleanVector function


## -description


Extracts a Boolean vector from a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -parameters




### -param propvar [in]

Type: <b>REFPROPVARIANT</b>

Reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param prgf [out]

Type: <b>BOOL*</b>

Points to a buffer that contains <i>crgf</i> <b>BOOL</b> values. When this function returns, the buffer has been initialized with <i>pcElem</i> Boolean elements extracted from the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param crgf [in]

Type: <b>ULONG</b>

Number of elements in the buffer pointed to by <i>prgf</i>.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains the count of Boolean elements extracted from source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


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
The source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> contained more than <i>crgf</i> values. The buffer pointed to by <i>prgf</i>.

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



This helper function is used when the calling application expects a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> to hold a Boolean vector value with a fixed number of elements.

If the source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> has type VT_VECTOR | VT_BOOL or VT_ARRAY | VT_BOOL, this helper function extracts up to <i>crgf</i> Boolean values an places them into the buffer pointed to by <i>prgf</i>. If the <b>PROPVARIANT</b> contains more elements than will fit into the <i>prgf</i> buffer, this function returns an error and sets <i>pcElem</i> to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776532(v=VS.85).aspx">PropVariantToBooleanVector</a> to access a Boolean vector stored in a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>.


```cpp
// PROPVARIANT propvar;
// Assume the variable propvar is initialized and valid.

// The application is expecting the propvar variable to hold 4 Booleans
// in a vector.
BOOL rgFlags[4]; 
ULONG cFlags;
HRESULT hr = PropVariantToBooleanVector(propvar, rgFlags, ARRAYSIZE(rgFlags), &cFlags);

if (SUCCEEDED(hr))
{
     if (cFlags == ARRAYSIZE(rgFlags))
     {
         // The application received 4 flags which are now stored in rgFlags.
     }
     else
     {
         // The application received cFlags flags which are now stored in the 
         // first cFlags elements of rgFlags.
     }
}
```




