---
UID: NF:oleauto.SafeArrayPutElement
title: SafeArrayPutElement function
author: windows-sdk-content
description: Stores the data element at the specified location in the array.
old-location: automat\safearrayputelement.htm
tech.root: automat
ms.assetid: 7c837b4f-d319-4d98-934a-b585fe521bf8
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: SafeArrayPutElement, SafeArrayPutElement function [Automation], _oa96_SafeArrayPutElement, automat.safearrayputelement, oleauto/SafeArrayPutElement
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
 - SafeArrayPutElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# SafeArrayPutElement function


## -description


Stores the data element at the specified location in the array.


## -parameters




### -param psa [in]

An array descriptor created by <a href="https://msdn.microsoft.com/5b94f1a2-a558-473f-85dd-9545c0464cc7">SafeArrayCreate</a>.



### -param rgIndices [in]

A vector of indexes for each dimension of the array. The right-most (least significant) dimension is rgIndices[0]. The left-most dimension is stored at <code>rgIndices[psa-&gt;cDims – 1]</code>.



### -param pv [in]

The data to assign to the array. The variant types VT_DISPATCH, VT_UNKNOWN, and VT_BSTR are pointers, and do not require another level of indirection.


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
<dt><b>DISP_E_BADINDEX</b></dt>
</dl>
</td>
<td width="60%">
The specified index is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Memory could not be allocated for the element.

</td>
</tr>
</table>
 




## -remarks



This function automatically calls <a href="https://msdn.microsoft.com/cb29d862-c7c5-4852-b017-c29e88d5f1c4">SafeArrayLock</a> and <a href="https://msdn.microsoft.com/654995ab-1959-44dc-9e26-11c34e489c14">SafeArrayUnlock</a> before and after assigning the element. If the data element is a string, object, or variant, the function copies it correctly when the safe array is destroyed. If the existing element is a string, object, or variant, it is cleared correctly.  If the data element is a VT_DISPATCH or VT_UNKNOWN, <b>AddRef</b> is called to increment the object's reference count. 

<div class="alert"><b>Note</b>  Multiple locks can be on an array. Elements can be put into an array while the array is locked by other operations.</div>
<div> </div>
For an example that demonstrates calling <b>SafeArrayPutElement</b>, see the COM Fundamentals Lines sample (CLines::Add in Lines.cpp).



