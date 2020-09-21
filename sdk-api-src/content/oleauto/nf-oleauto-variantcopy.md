---
UID: NF:oleauto.VariantCopy
title: VariantCopy function (oleauto.h)
description: Frees the destination variant and makes a copy of the source variant.
helpviewer_keywords: ["VariantCopy","VariantCopy function [Automation]","_oa96_VariantCopy","automat.variantcopy","oleauto/VariantCopy"]
old-location: automat\variantcopy.htm
tech.root: automat
ms.assetid: f6ddbe1f-37b0-44f1-a3f0-b7ef4df88f8a
ms.date: 12/05/2018
ms.keywords: VariantCopy, VariantCopy function [Automation], _oa96_VariantCopy, automat.variantcopy, oleauto/VariantCopy
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
 - VariantCopy
 - oleauto/VariantCopy
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
 - VariantCopy
---

# VariantCopy function


## -description

Frees the destination variant and makes a copy of the source variant.

## -parameters

### -param pvargDest [out]

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

First, free any memory that is owned by pvargDest, such as <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantclear">VariantClear</a> (pvargDest must point to a valid initialized variant, and not simply to an uninitialized memory location). Then pvargDest receives an exact copy of the contents of pvargSrc. 

If pvargSrc is a VT_BSTR, a copy of the string is made. If pvargSrcis a VT_ARRAY, the entire array is copied. If pvargSrc is a VT_DISPATCH or VT_UNKNOWN, <b>AddRef</b> is called to increment the object's reference count.

If the variant to be copied is a COM object that is passed by reference, the vtfield of the pvargSrcparameter is VT_DISPATCH | VT_BYREF or VT_UNKNOWN | VT_BYREF.  In this case, <b>VariantCopy</b> does not increment the reference count on the referenced object. Because the variant being copied is a pointer to a reference to an object, <b>VariantCopy</b> has no way to determine if it is necessary to increment the reference count of the object. It is therefore the responsibility of the caller to call <b>IUnknown::AddRef</b> on the object or not, as appropriate. 

<div class="alert"><b>Note</b>  The <b>VariantCopy</b> method is not threadsafe.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/automat/variant-manipulation-functions">Variant Manipulation Functions</a>