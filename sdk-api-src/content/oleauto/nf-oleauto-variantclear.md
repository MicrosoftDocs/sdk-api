---
UID: NF:oleauto.VariantClear
title: VariantClear function (oleauto.h)
description: Clears a variant.
helpviewer_keywords: ["VariantClear","VariantClear function [Automation]","_oa96_VariantClear","automat.variantclear","oleauto/VariantClear"]
old-location: automat\variantclear.htm
tech.root: automat
ms.assetid: 28741d81-8404-4f85-95d3-5c209ec13835
ms.date: 12/05/2018
ms.keywords: VariantClear, VariantClear function [Automation], _oa96_VariantClear, automat.variantclear, oleauto/VariantClear
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
 - VariantClear
 - oleauto/VariantClear
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
 - VariantClear
---

# VariantClear function


## -description

Clears a variant.

## -parameters

### -param pvarg [in, out]

The variant to clear.

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
</table>

## -remarks

Use this function to clear variables of type VARIANTARG (or VARIANT) before the memory containing the VARIANTARG is freed (as when a local variable goes out of scope). 

The function clears a VARIANTARG by setting the vt field to VT_EMPTY. The current contents of the VARIANTARG are released first. If the vtfield is VT_BSTR, the string is freed. If the vtfield is VT_DISPATCH, the object is released. If the vt field has the VT_ARRAY bit set, the array is freed.

If the variant to be cleared is a COM object that is passed by reference, the vtfield of the pvargparameter is VT_DISPATCH | VT_BYREF or VT_UNKNOWN | VT_BYREF.  In this case, <b>VariantClear</b> does not release the object. Because the variant being cleared is a pointer to a reference to an object, <b>VariantClear</b> has no way to determine if it is necessary to release the object. It is therefore the responsibility of the caller to release the object or not, as appropriate. 

In certain cases, it may be preferable to clear a variant in code without calling <b>VariantClear</b>. For example, you can change the type of a VT_I4 variant to another type without calling this function. Safearrays of BSTR will have <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> called on each element not <b>VariantClear</b>. However, you must call <b>VariantClear</b> if a VT_type is received but cannot be handled. Safearrays of variant will also have <b>VariantClear</b> called on each member. Using <b>VariantClear</b> in these cases ensures that code will continue to work if Automation adds new variant types in the future.

Do not use <b>VariantClear</b> on uninitialized variants; use <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantinit">VariantInit</a> to initialize a new VARIANTARG or VARIANT.

Variants containing arrays with outstanding references cannot be cleared.  Attempts to do so will return an HRESULT containing DISP_E_ARRAYISLOCKED.


#### Examples

The following example shows how to clear an array of variants, where <code>celt</code> is the number of elements in the array.


```cpp
for(int i = 0; i < celt; ++i)
   VariantClear(&rgvar[i]);
```

## -see-also

<a href="/previous-versions/windows/desktop/automat/variant-manipulation-functions">Variant Manipulation Functions</a>