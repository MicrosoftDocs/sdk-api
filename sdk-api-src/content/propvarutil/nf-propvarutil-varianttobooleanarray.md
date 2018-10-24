---
UID: NF:propvarutil.VariantToBooleanArray
title: VariantToBooleanArray function
author: windows-sdk-content
description: Extracts an array of Boolean values from a VARIANT structure.
old-location: properties\VariantToBooleanArray.htm
tech.root: properties
ms.assetid: 80a1e7d4-ec11-4b16-ba05-b97f3bbf02d0
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: VariantToBooleanArray, VariantToBooleanArray function [Windows Properties], _shell_VariantToBooleanArray, properties.VariantToBooleanArray, propvarutil/VariantToBooleanArray, shell.VariantToBooleanArray
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
 - VariantToBooleanArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Desktop Search (WDS) 3.0
---

# VariantToBooleanArray function


## -description


Extracts an array of Boolean values from a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -parameters




### -param var [in]

Type: <b>REFVARIANT</b>

Reference to a source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


### -param prgf [out]

Type: <b>BOOL*</b>

Pointer to a buffer that contains <i>crgn</i> Boolean values. When this function returns, the buffer has been initialized with *<i>pcElem</i> <b>BOOL</b> elements extracted from the source  <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


### -param crgn [in]

Type: <b>ULONG</b>

The number of elements in the buffer pointed to by <i>prgf</i>.


### -param pcElem [out]

Type: <b>ULONG*</b>

When this function returns, contains a pointer to the count of <b>BOOL</b> elements extracted from the source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise, including the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_BUFFERTOOSMALL</b></dt>
</dl>
</td>
<td width="60%">
The source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> contained more than <i>crgn</i> values.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> was not of the appropriate type.

</td>
</tr>
</table>
 




## -remarks



This helper function is used when the calling application expects a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> to hold an array that consists of a fixed number of Boolean values.

If the source <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> is of type VT_ARRAY | VT_BOOL, this function extracts up to <i>crgn</i> <b>BOOL</b> values and places them into the buffer pointed to by <i>prgf</i>. If the <b>VARIANT</b> contains more elements than will fit into the <i>prgf</i> buffer, this function returns an error and sets *<i>pcElem</i> to 0.


#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="shell.VariantToBooleanArray">VariantToBooleanArray</a> to access an array of <b>BOOL</b> values stored in a <a href="e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a> structure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// VARIANT var;
// Assume variable var is initialized and valid
BOOL rgFlags[4]; // The application is expecting var to hold 4 BOOLs in an array.
ULONG cFlags;

HRESULT hr = VariantToBooleanArray(var, rgFlags, ARRAYSIZE(rgFlags), &amp;cFlags);

if (SUCCEEDED(hr))
{
    if (cFlags == ARRAYSIZE(rgFlags))
    {
        // The application got 4 flag values which are now stored in rgFlags.
    }
    else
    {
        // The application got cFlags which are stored in the first cFlags 
        // elements of rgFlags.
    }
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="shell.InitVariantFromBooleanArray">InitVariantFromBooleanArray</a>



<a href="shell.PropVariantToBooleanVector">PropVariantToBooleanVector</a>



<a href="shell.VariantGetBooleanElem">VariantGetBooleanElem</a>



<a href="shell.VariantToBoolean">VariantToBoolean</a>



<a href="shell.VariantToBooleanArrayAlloc">VariantToBooleanArrayAlloc</a>
 

 

