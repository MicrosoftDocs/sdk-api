---
UID: NF:oleauto.VariantCopyInd
title: VariantCopyInd function
author: windows-sdk-content
description: Frees the destination variant and makes a copy of the source variant, performing the necessary indirection if the source is specified to be VT_BYREF.
old-location: automat\variantcopyind.htm
tech.root: automat
ms.assetid: 5d9be6cd-92e5-485c-ba0d-8630d3e414b8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: VariantCopyInd, VariantCopyInd function [Automation], _oa96_VariantCopyInd, automat.variantcopyind, oleauto/VariantCopyInd
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
 - VariantCopyInd
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# VariantCopyInd function


## -description


Frees the destination variant and makes a copy of the source variant, performing the necessary indirection if the source is specified to be VT_BYREF.


## -parameters




### -param pvarDest [out]

The destination variant.


### -param pvargSrc [in]

The source variant.


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
<dt><b>DISP_E_ARRAYISLOCKED</b></dt>
</dl>
</td>
<td width="60%">
The variant contains an array that is locked.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_BADVARTYPE</b></dt>
</dl>
</td>
<td width="60%">
The variant type is not a valid type of variant.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG
</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY
</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
</table>
 




## -remarks



This function is useful when a copy of a variant is needed, and to guarantee that it is not VT_BYREF, such as when handling arguments in an implementation of <a href="https://msdn.microsoft.com/en-us/library/ms221479(v=VS.85).aspx">IDispatch::Invoke</a>.

For example, if the source is a (VT_BYREF | VT_I2), the destination will be a BYVAL | VT_I2. The same is true for all legal VT_BYREF combinations, including VT_VARIANT.

If pvargSrc is (VT_BYREF | VT_VARIANT), and the contained variant is VT_BYREF, the contained variant is also dereferenced.

This function frees any existing contents of pvarDest.




## -see-also




<a href="https://msdn.microsoft.com/f0940eea-077f-4b68-9dac-d49e3fc62e43">Variant Manipulation Functions</a>
 

 

