---
UID: NF:propsys.IPropertyDescription.CoerceToCanonicalValue
title: IPropertyDescription::CoerceToCanonicalValue (propsys.h)
description: Coerces the value to the canonical value, according to the property description.
old-location: properties\IPropertyDescription_CoerceToCanonicalValue.htm
tech.root: properties
ms.assetid: bc51ec1b-c1ec-4162-a60d-b67d19d5b591
ms.date: 12/05/2018
ms.keywords: CoerceToCanonicalValue, CoerceToCanonicalValue method [Windows Properties], CoerceToCanonicalValue method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],CoerceToCanonicalValue method, IPropertyDescription.CoerceToCanonicalValue, IPropertyDescription::CoerceToCanonicalValue, properties.IPropertyDescription_CoerceToCanonicalValue, propsys/IPropertyDescription::CoerceToCanonicalValue, shell.IPropertyDescription_CoerceToCanonicalValue, shell_IPropertyDescription_CoerceToCanonicalValue
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPropertyDescription::CoerceToCanonicalValue
 - propsys/IPropertyDescription::CoerceToCanonicalValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescription.CoerceToCanonicalValue
---

# IPropertyDescription::CoerceToCanonicalValue


## -description

Coerces the value to the canonical value, according to the property description.

## -parameters

### -param ppropvar [in, out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>*</b>

On entry, contains a pointer to a <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure that contains the original value. When this method returns, contains the canonical value.

## -returns

Type: <b>HRESULT</b>

If the failure code is not INPLACE_S_TRUNCATED or E_INVALIDARG, then coercion from the value's type to the property description's type was not possible, and the <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure has been cleared.

                    

Possible results include the following:

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
The function succeeded. The property value specified by <i>ppropvar</i> is now in a canonical form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>INPLACE_S_TRUNCATED</b></dt>
</dl>
</td>
<td width="60%">
The property value specified by <i>ppropvar</i> is now in a truncated, canonical form.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppropvar</i> parameter is invalid. The <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure has been cleared.

</td>
</tr>
</table>

## -remarks

For more information, see the <i>type</i> attribute of the <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> element in the property's .propdesc file.

Most property descriptions specify the type that their values are expected to use.  For example, the property description for <a href="/windows/desktop/properties/props-system-title">System.Title</a> specifies that System.Title values should use <code>VT_LPWSTR</code>. This method coerces values to this type, and coerces the result into a canonical form.

It is important to note that if this method fails, it will have already called the <a href="/previous-versions/windows/desktop/oe/oe-imimeallocator-propvariantclear">PropVariantClear</a> on the input <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structure. Only if this method succeeds is the calling application responsible for calling the <b>PropVariantClear</b> on <i>ppropvar</i> when the structure is no longer needed.

The coercion performed by this method is also performed by the property system during  <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-getvalue">IPropertyStore::GetValue</a>  and <a href="/windows/desktop/api/propsys/nf-propsys-ipropertystore-setvalue">IPropertyStore::SetValue</a> calls. Applications may depend on the property system to perform the coercions, or may use this method to perform the coercion at a time of the application's choosing.

The coercion is performed in four steps, as follows:
                

<ol>
<li>The following values are converted to <code>VT_EMPTY</code>.
                        <ul>
<li>Values of type <code>VT_NULL</code>.</li>
<li>Values of type <code>VT_LPWSTR, VT_BSTR</code>, or <code>VT_LPSTR</code> whose pointer is <b>NULL</b>.</li>
<li>Values of type <code>VT_LPWSTR, VT_BSTR</code>, or <code>VT_LPSTR</code> that are empty or consist entirely of spaces.</li>
<li>Values of type <code>VT_FILETIME</code> prior to midnight 1601/01/02.</li>
</ul>
</li>
<li>If the value is not of type <code>VT_EMPTY</code> after Step 1, it is converted to the type specified by the property description.  The type of a property description can be obtained using <a href="/windows/desktop/api/propsys/nf-propsys-ipropertydescription-getpropertytype">IPropertyDescription::GetPropertyType</a>. See <a href="/windows/desktop/properties/propdesc-schema-typeinfo">typeInfo</a> for information about how the property schema influences the type of a property description. Conversions are performed as follows:
                        <ul>
<li>Values of type <code>VT_LPWSTR, VT_BSTR</code>, or <code>VT_LPSTR</code> are converted to <code>VT_VECTOR | VT_LPWSTR</code> using <a href="/windows/desktop/api/propvarutil/nf-propvarutil-initpropvariantfromstringasvector">InitPropVariantFromStringAsVector</a>.</li>
<li>All other conversions are performed using <a href="/windows/desktop/api/propvarutil/nf-propvarutil-propvariantchangetype">PropVariantChangeType</a>
</li>
</ul>
</li>
<li>After Steps 2 and 3, the value is coerced into a canonical form based on its type. The canonical forms are summarized in the following table.

<table class="clsStd">
<tr>
<th>Value Type</th>
<th>Canonical Form</th>
</tr>
<tr>
<td><code>VT_EMPTY</code></td>
<td>Always canonical.</td>
</tr>
<tr>
<td><code>VT_LPWSTR</code></td>
<td>
<ul>
<li>No leading or trailing spaces. The string is non-empty. The string is non-<b>NULL</b>. For example, <code>L"Alice"</code>.</li>
<li>If this is a tree property (that is, if the typeInfo element's <code>isTreeProperty</code> attribute is <b>TRUE</b>), then it must not have leading or trailing forward slashes (/), must not have spaces between the text and the forward slashes, and must not have two consecutive forward slashes(/). For example, <code>L"Friend/Bob"</code></li>
<li>Coercion removes unnecessary characters and will result in <code>VT_EMPTY</code> if there was no content.</li>
</ul>
</td>
</tr>
<tr>
<td><code>VT_VECTOR | VT_LPWSTR</code></td>
<td>
<ul>
<li>Each string in the vector must adhere to the rules for <code>VT_LPWSTR</code> listed above. In addition, the vector must have no duplicates and have no null pointers.</li>
<li>If this is a tree property, then no value can be the ancestor of another value. For example, <code>L"Friend"</code> is an ancestor of L"Friend/Bob".</li>
<li>If there is no content, coercion removes duplicate and ancestor characters and will result in <code>VT_EMPTY</code>.</li>
</ul>
</td>
</tr>
</table>
 

</li>
<li>If applicable, the value is checked against the property description type enumeration.  The following checks apply.

<table class="clsStd">
<tr>
<th>Enumeration Type</th>
<th>Value Type</th>
<th>Canonical Form</th>
</tr>
<tr>
<td>Discrete or Ranged</td>
<td><code>VT_EMPTY</code></td>
<td>Always canonical</td>
</tr>
<tr>
<td>Discrete</td>
<td><code>VT_LPWSTR</code></td>
<td>The string matches one of the enumerated strings allowed for the property. Comparisons are case-insensitive. If not, convert the value to <code>VT_EMPTY</code>.</td>
</tr>
<tr>
<td>Discrete</td>
<td>Numeric</td>
<td>The number matches one of the enumerated values allowed for the property. If not, convert the value to <code>VT_EMPTY</code>.</td>
</tr>
<tr>
<td>Discrete</td>
<td><code>VT_VECTOR | VT_LPWSTR</code></td>
<td>Each string in the vector matches one of the enumerated strings allowed for the property. Comparisons are case-insensitive. If not, remove that string from the vector. If the resulting vector is empty, convert the value to <code>VT_EMPTY</code>.</td>
</tr>
<tr>
<td>Discrete</td>
<td><code>VT_VECTOR |</code> Numeric</td>
<td>Each number in the vector matches one of the enumerated values allowed for the property. If not, remove that number from the vector. If the resulting vector is empty, convert the value to <code>VT_EMPTY</code>.</td>
</tr>
<tr>
<td>Ranged</td>
<td><code>VT_LPWSTR</code></td>
<td>The string exists in the range allowed for the property. Comparisons are case-sensitive. If not, convert the value to <code>VT_EMPTY</code>.</td>
</tr>
<tr>
<td>Ranged</td>
<td>Numeric</td>
<td>The number exists in the range allowed for the property. If not, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Ranged</td>
<td><code>VT_VECTOR | VT_LPWSTR</code></td>
<td>Each string in the vector exists in the range allowed for the property.  Comparisons are case-sensitive. If not, remove that string from the vector. If the resulting vector is empty, convert the value to <code>VT_EMPTY</code>.</td>
</tr>
<tr>
<td>Ranged</td>
<td><code>VT_VECTOR</code> | Numeric</td>
<td>Each number in the vector exists in the range allowed for the property. If not, remove that number from the vector. If the resulting vector is empty, convert the value to VT_EMPTY.</td>
</tr>
</table>
 

</li>
</ol>

## -see-also

<a href="/windows/desktop/api/propsys/nn-propsys-ipropertydescription">IPropertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-entry">Property Description Schema</a>