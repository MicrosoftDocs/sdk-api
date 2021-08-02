---
UID: NF:oleauto.VariantChangeType
title: VariantChangeType function (oleauto.h)
description: Converts a variant from one type to another.
helpviewer_keywords: ["VARIANT_ALPHABOOL","VARIANT_LOCALBOOL","VARIANT_NOUSEROVERRIDE","VARIANT_NOVALUEPROP","VariantChangeType","VariantChangeType function [Automation]","_oa96_VariantChangeType","automat.variantchangetype","oleauto/VariantChangeType"]
old-location: automat\variantchangetype.htm
tech.root: automat
ms.assetid: 48a51e32-95d7-4eeb-8106-f5043ffa2fd1
ms.date: 12/05/2018
ms.keywords: VARIANT_ALPHABOOL, VARIANT_LOCALBOOL, VARIANT_NOUSEROVERRIDE, VARIANT_NOVALUEPROP, VariantChangeType, VariantChangeType function [Automation], _oa96_VariantChangeType, automat.variantchangetype, oleauto/VariantChangeType
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
 - VariantChangeType
 - oleauto/VariantChangeType
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
 - VariantChangeType
---

## -description

> [!IMPORTANT]
> This API is affected by the problem described in Microsoft Support topic [VarI8FromCy produces incorrect value when CY value is very large](https://support.microsoft.com/help/2282810).

Converts a variant from one type to another.

## -parameters

### -param pvargDest [out]

The destination variant. If this is the same as <i>pvarSrc</i>, the variant will be converted in place.

### -param pvarSrc [in]

The variant to convert.

### -param wFlags [in]

Flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="VARIANT_NOVALUEPROP"></a><a id="variant_novalueprop"></a><dl>
<dt><b>VARIANT_NOVALUEPROP</b></dt>
</dl>
</td>
<td width="60%">
Prevents the function from attempting to coerce an object to a fundamental type by getting the Value property. Applications should set this flag only if necessary, because it makes their behavior inconsistent with other applications.

</td>
</tr>
<tr>
<td width="40%"><a id="VARIANT_ALPHABOOL"></a><a id="variant_alphabool"></a><dl>
<dt><b>VARIANT_ALPHABOOL</b></dt>
</dl>
</td>
<td width="60%">
Converts a VT_BOOL value to a string containing either "True" or "False". 


</td>
</tr>
<tr>
<td width="40%"><a id="VARIANT_NOUSEROVERRIDE"></a><a id="variant_nouseroverride"></a><dl>
<dt><b>VARIANT_NOUSEROVERRIDE</b></dt>
</dl>
</td>
<td width="60%">
For conversions to or from VT_BSTR, passes LOCALE_NOUSEROVERRIDE to the core coercion routines. 


</td>
</tr>
<tr>
<td width="40%"><a id="VARIANT_LOCALBOOL"></a><a id="variant_localbool"></a><dl>
<dt><b>VARIANT_LOCALBOOL</b></dt>
</dl>
</td>
<td width="60%">
For conversions from VT_BOOL to VT_BSTR and back, uses the language specified by the locale in use on the local computer. 

</td>
</tr>
</table>

### -param vt [in]

The type to convert to. If the return code is S_OK, the <b>vt</b> field of the *<i>pvargDest</i> is guaranteed to be equal to this value.

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
<dt><b>DISP_E_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The data pointed to by <i>pvarSrc</i> does not fit in the destination type.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>DISP_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The argument could not be coerced to the specified type.

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

The <b>VariantChangeType</b> function handles coercions between the fundamental types (including numeric-to-string and string-to-numeric coercions). The <i>pvarSrc</i> argument is changed during the conversion process. For example, if the source variant is of type VT_BOOL and the destination is of type VT_UINT, the <i>pvarSrc</i> argument is first converted to VT_I2 and then the conversion proceeds. A variant that has VT_BYREF set is coerced to a value by obtaining the referenced value. An object is coerced to a value by invoking the object's <b>Value</b> property (DISPID_VALUE). 

Typically, the implementer of <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">IDispatch::Invoke</a> determines which member is being accessed, and then calls <b>VariantChangeType</b> to get the value of one or more arguments. For example, if the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> call specifies a <b>SetTitle</b> member that takes one string argument, the implementer would call <b>VariantChangeType</b> to attempt to coerce the argument to VT_BSTR. If <b>VariantChangeType</b> does not return an error, the argument could then be obtained directly from the <b>bstrVal</b> field of the VARIANTARG. If <b>VariantChangeType</b> returns DISP_E_TYPEMISMATCH, the implementer would set *<i>puArgErr</i> to 0 (indicating the argument in error) and return DISP_E_TYPEMISMATCH from <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-idispatch-invoke">Invoke</a>.

Arrays of one type cannot be converted to arrays of another type with this function.

<div class="alert"><b>Note</b>  The type of a VARIANTARG should not be changed in the <i>rgvarg</i> array in place.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/automat/variant-manipulation-functions">Variant Manipulation Functions</a>



<a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-variantchangetypeex">VariantChangeTypeEx</a>