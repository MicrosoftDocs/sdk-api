---
UID: NF:propsys.PSCoerceToCanonicalValue
title: PSCoerceToCanonicalValue function
author: windows-sdk-content
description: Converts the value of a property to the canonical value, according to the property description.
old-location: properties\PSCoerceToCanonicalValue.htm
old-project: properties
ms.assetid: 8225dd01-47cc-451e-b6a6-c16ddf62ca20
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PSCoerceToCanonicalValue, PSCoerceToCanonicalValue function [Windows Properties], _shell_PSCoerceToCanonicalValue, properties.PSCoerceToCanonicalValue, propsys/PSCoerceToCanonicalValue, shell.PSCoerceToCanonicalValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: propsys.h
req.include-header: 
req.redist: Windows Desktop Search (WDS) 3.0
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
tech.root: 
req.typenames: PSC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Propsys.dll
api_name:
 - PSCoerceToCanonicalValue
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: ADAM
---

# PSCoerceToCanonicalValue function


## -description


Converts the value of a property to the canonical value, according to the property description.


## -parameters




### -param key [in]

Type: <b>REFPROPERTYKEY</b>

Reference to a <a href="https://msdn.microsoft.com/en-us/library/Bb773381(v=VS.85).aspx">PROPERTYKEY</a> structure that identifies the property whose value is to be coerced.


### -param ppropvar [in, out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

On entry, contains a pointer to a <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure that contains the original value. When this function returns successfully, contains the canonical value.


## -returns



Type: <b>HRESULT</b>

Possible return values include the following:

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
The <i>ppropvar</i> parameter is invalid. The <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure has been cleared.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TYPE_E_TYPEMISMATCH</b></dt>
</dl>
</td>
<td width="60%">
Coercion from the value's type to the property description's type was not possible. The <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure has been cleared.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Any other failure code</b></dt>
</dl>
</td>
<td width="60%">
Coercion from the value's type to the property description's type was not possible. The <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure has been cleared.

</td>
</tr>
</table>
 




## -remarks



This function is a wrapper around the system's implementation of <a href="https://msdn.microsoft.com/library/Bb761519(v=VS.85).aspx">IPropertyDescription::CoerceToCanonicalValue</a>.

Most property descriptions specify the type that their values are expected to use. For example, the property description for <a href="https://msdn.microsoft.com/en-us/library/Bb787584(v=VS.85).aspx">System.Title</a> specifies that System.Title values should be of type VT_LPWSTR. This function coerces values to this type, and then coerces the result into a canonical form.

It is important to note that if this function fails, it will have already called <a href="https://msdn.microsoft.com/en-us/library/ms712573(v=VS.85).aspx">PropVariantClear</a> on the input <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure. Only if this function succeeds is the calling application responsible for calling <b>PropVariantClear</b> on <i>ppropvar</i> when the structure is no longer needed.

The coercion performed by this function is also performed by the property system during calls to <a href="https://msdn.microsoft.com/en-us/library/Ff536962(v=VS.85).aspx">IPropertyStore::GetValue</a> and <a href="https://msdn.microsoft.com/en-us/library/Ff536963(v=VS.85).aspx">IPropertyStore::SetValue</a>. Applications can either depend on the property system to perform the coercions or can use this function to perform the coercion at a time of the application's choosing.

The coercion is performed in four steps, as follows:
        
                

<ol>
<li>The following values are converted to VT_EMPTY.
                        <ul>
<li>Values of type VT_NULL.</li>
<li>Values of type VT_LPWSTR, VT_BSTR, or VT_LPSTR whose pointer is <b>NULL</b>.</li>
<li>Values of type VT_LPWSTR, VT_BSTR, or VT_LPSTR that are empty or consist entirely of spaces.</li>
<li>Values of type VT_FILETIME prior to midnight 1601/01/02.</li>
</ul>
</li>
<li>If the value is not of type VT_EMPTY after Step 1, it is converted to the type specified by the property description. The type of a property description can be obtained by calling <a href="https://msdn.microsoft.com/library/Bb761545(v=VS.85).aspx">IPropertyDescription::GetPropertyType</a>. For information on how the property schema influences the type of a property description, see <a href="https://msdn.microsoft.com/en-us/library/Bb773889(v=VS.85).aspx">typeInfo</a>. Conversions are performed as follows:
                        
                        <ul>
<li>Values of type VT_LPWSTR, VT_BSTR, or VT_LPSTR are converted to VT_VECTOR | VT_LPWSTR using <a href="https://msdn.microsoft.com/en-us/library/Bb762306(v=VS.85).aspx">InitPropVariantFromStringAsVector</a>.</li>
<li>All other conversions are performed using <a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>
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
<td>VT_EMPTY</td>
<td>Always canonical.</td>
</tr>
<tr>
<td>VT_LPWSTR</td>
<td>
<ul>
<li>No leading or trailing spaces. The string is non-empty and non-<b>NULL</b>. For example, L"Alice".</li>
<li>If this is a tree property (that is, if the <a href="https://msdn.microsoft.com/en-us/library/Bb773889(v=VS.85).aspx">typeInfo</a> element's <i>isTreeProperty</i> attribute is <b>TRUE</b>), then it must not have leading or trailing forward slashes (/), must not have spaces between the text and the forward slashes, and must not have two consecutive forward slashes(/). For example, L"Friend/Bob".</li>
<li>Coercion removes unnecessary characters and results in VT_EMPTY if there was no content.</li>
</ul>
</td>
</tr>
<tr>
<td>VT_VECTOR | VT_LPWSTR</td>
<td>
<ul>
<li>Each string in the vector must adhere to the rules for VT_LPWSTR listed above. In addition, the vector must have no duplicates and have no null pointers.</li>
<li>If this is a tree property, then no value can be the ancestor of another value. For example, L"Friend" is an ancestor of L"Friend/Bob".</li>
<li>If there is no content, coercion removes duplicate and ancestor characters and results in VT_EMPTY.</li>
</ul>
</td>
</tr>
</table>
 

</li>
<li>If applicable, the value is checked against the property description type enumeration.  The checks in the following table apply.

<table class="clsStd">
<tr>
<th>Enumeration Type</th>
<th>Value Type</th>
<th>Canonical Form</th>
</tr>
<tr>
<td>Discrete or Ranged</td>
<td>VT_EMPTY</td>
<td>Always canonical</td>
</tr>
<tr>
<td>Discrete</td>
<td>VT_LPWSTR</td>
<td>The string matches one of the enumerated strings allowed for the property. Comparisons are case-insensitive. If not, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Discrete</td>
<td>Numeric</td>
<td>The number matches one of the enumerated values allowed for the property. If not, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Discrete</td>
<td>VT_VECTOR | VT_LPWSTR</td>
<td>Each string in the vector matches one of the enumerated strings allowed for the property. Comparisons are case-insensitive. If not, remove that string from the vector. If the resulting vector is empty, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Discrete</td>
<td>VT_VECTOR | Numeric</td>
<td>Each number in the vector matches one of the enumerated values allowed for the property. If not, remove that number from the vector. If the resulting vector is empty, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Ranged</td>
<td>VT_LPWSTR</td>
<td>The string exists in the range allowed for the property. Comparisons are case-sensitive. If not, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Ranged</td>
<td>Numeric</td>
<td>The number exists in the range allowed for the property. If not, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Ranged</td>
<td>VT_VECTOR | VT_LPWSTR</td>
<td>Each string in the vector exists in the range allowed for the property. Comparisons are case-sensitive. If not, remove that string from the vector. If the resulting vector is empty, convert the value to VT_EMPTY.</td>
</tr>
<tr>
<td>Ranged</td>
<td>VT_VECTOR | Numeric</td>
<td>Each number in the vector exists in the range allowed for the property. If not, remove that number from the vector. If the resulting vector is empty, convert the value to VT_EMPTY.</td>
</tr>
</table>
 

</li>
</ol>

#### Examples

The following example, to be included as part of a larger program, demonstrates how to use <a href="https://msdn.microsoft.com/en-us/library/Bb776486(v=VS.85).aspx">PSCoerceToCanonicalValue</a> to coerce a value to the type required for PKEY_Keywords.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// PROPVARIANT propvar;
// Assume variable propvar is initialized and valid.

HRESULT hr = PSCoerceToCanonicalValue(PKEY_Keywords, &amp;propvar);

if (SUCCEEDED(hr))
{
    // The conversion succeeded and propvar now is of the correct type for 
    // PKEY_Keywords, or VT_EMPTY.
    PropVariantClear(&amp;propvar);
}
else
{
    // The conversion failed and propvar is now VT_EMPTY.
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/706b2551-a9b0-4368-babb-e54cea6d297e">IShellItem2::GetPropertyStore</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb776514(v=VS.85).aspx">PropVariantChangeType</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773889(v=VS.85).aspx">typeInfo</a>
 

 

