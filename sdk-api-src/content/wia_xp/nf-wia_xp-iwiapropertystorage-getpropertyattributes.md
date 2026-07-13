---
UID: NF:wia_xp.IWiaPropertyStorage.GetPropertyAttributes
title: IWiaPropertyStorage::GetPropertyAttributes (wia_xp.h)
description: The IWiaPropertyStorage::GetPropertyAttributes method retrieves access rights and legal value information for a specified set of properties.
helpviewer_keywords: ["GetPropertyAttributes","GetPropertyAttributes method [WIA]","GetPropertyAttributes method [WIA]","IWiaPropertyStorage interface","IWiaPropertyStorage interface [WIA]","GetPropertyAttributes method","IWiaPropertyStorage.GetPropertyAttributes","IWiaPropertyStorage::GetPropertyAttributes","_wia_IWiaPropertyStorage_GetPropertyAttributes","wia._wia_IWiaPropertyStorage_GetPropertyAttributes","wia_xp/IWiaPropertyStorage::GetPropertyAttributes"]
old-location: wia\_wia_IWiaPropertyStorage_GetPropertyAttributes.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\iwiapropertystorage\getpropertyattributes.htm
ms.date: 12/05/2018
ms.keywords: GetPropertyAttributes, GetPropertyAttributes method [WIA], GetPropertyAttributes method [WIA],IWiaPropertyStorage interface, IWiaPropertyStorage interface [WIA],GetPropertyAttributes method, IWiaPropertyStorage.GetPropertyAttributes, IWiaPropertyStorage::GetPropertyAttributes, _wia_IWiaPropertyStorage_GetPropertyAttributes, wia._wia_IWiaPropertyStorage_GetPropertyAttributes, wia_xp/IWiaPropertyStorage::GetPropertyAttributes
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wiaguid.lib
req.dll: Wiaservc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWiaPropertyStorage::GetPropertyAttributes
 - wia_xp/IWiaPropertyStorage::GetPropertyAttributes
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaservc.dll
api_name:
 - IWiaPropertyStorage.GetPropertyAttributes
archived: true
---

# IWiaPropertyStorage::GetPropertyAttributes


## -description

The <b>IWiaPropertyStorage::GetPropertyAttributes</b> method retrieves access rights and legal value information for a specified set of properties.

## -parameters

### -param cpspec [in]

Type: <b>ULONG</b>

Specifies the number of property attributes to query.

### -param rgpspec [in]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propspec">PROPSPEC</a>[]</b>

Specifies an array of <a href="/windows/desktop/wia/-wia-wiadeviceinfoprop">Device Information Property Constants</a>. Each constant in the array selects a property to query.

### -param rgflags [out]

Type: <b>ULONG[]</b>

An array that receives a <a href="/windows/desktop/wia/-wia-property-attributes">property attribute descriptor</a> for each property specified in the <i>rgpspec</i> array. Each element in the array is one or more descriptor values combined with a bitwise <b>OR</b> operation.

### -param rgpropvar [out]

Type: <b><a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>[]</b>

An array that receives a <a href="/windows/desktop/wia/-wia-property-attributes">property attribute descriptor</a> for each property specified in the <i>pPROPSPEC</i> array. For more information, see <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a>.

## -returns

Type: <b>HRESULT</b>

This method returns one of the following values or a standard COM error code:

<table class="clsStd">
<tr>
<th>Return Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>S_OK</td>
<td>This method succeeded.</td>
</tr>
<tr>
<td>S_FALSE</td>
<td>The specified property names do not exist. No attributes were retrieved.</td>
</tr>
<tr>
<td>STG_E_ACCESSDENIED</td>
<td>The application does not have access to the property stream or the stream may already be open.</td>
</tr>
<tr>
<td>STG_E_INSUFFICIENTMEMORY</td>
<td>There is not enough memory to complete the operation.</td>
</tr>
<tr>
<td>ERROR_NOT_SUPPORTED</td>
<td>The property type is not supported.</td>
</tr>
<tr>
<td>STG_E_INVALIDPARAMETER</td>
<td>One or more parameters are invalid. One or more of the <a href="/windows/desktop/api/propidl/ns-propidl-propspec">PROPSPEC</a> structures contain invalid data.</td>
</tr>
<tr>
<td>STG_E_INVALIDPOINTER</td>
<td>One or more of the pointers passed to this method are invalid.</td>
</tr>
<tr>
<td>ERROR_NO_UNICODE_TRANSLATION</td>
<td>A translation from Unicode to ANSI or ANSI to Unicode failed.</td>
</tr>
</table>

## -remarks

This method retrieves both property access rights and valid property values. Access rights report whether the property is readable, writable, or both. Valid property values are specified as a range of values, a list of values, or a group of flag values. For more information, see <a href="/windows/desktop/wia/-wia-property-attributes">Property Attributes</a>.

If the property access rights flag has the <b>WIA_PROP_NONE</b> bit set, no legal value information is available for this property. Read only properties and properties with a binary data type are examples of properties that would have the <b>WIA_PROP_NONE</b> bit set.

If the property has a range of valid values, they can be determined through the <i>rgpropvar</i> parameter upon completion of this method. The <i>ppvValidValues</i> parameter specifies an array of <a href="/windows/desktop/api/propidl/ns-propidl-propvariant">PROPVARIANT</a> structures. 

For example, if the property range is specified as VT_VECTOR | VT_UI4, range information can be retrieved through the structure member 

<i>rgpropvar</i>[<i>n</i>].caul.pElems[<i>range_specifier</i>]

where <i>n</i> is the index number of the property that is inspected and <i>range_specifier</i> is one of the following:

<table class="clsStd">
<tr>
<th>Range Specifier</th>
<th>Meaning</th>
</tr>
<tr>
<td>WIA_RANGE_MAX</td>
<td>Maximum value to which the property may be set.</td>
</tr>
<tr>
<td>WIA_RANGE_MIN</td>
<td>Minimum value to which the property may be set.</td>
</tr>
<tr>
<td>WIA_RANGE_NOM</td>
<td>Normal or default property value.</td>
</tr>
<tr>
<td>WIA_RANGE_STEP</td>
<td>Increment or decrement between property values.</td>
</tr>
</table>
 

If the property has a list of valid values, applications determine them through the <i>ppvValidValues</i> parameter upon completion of this method. 

For example, if the property range is specified as VT_VECTOR | VT_UI4, the list of valid property values can be retrieved through the structure member 

rgpropspecValues[<i>n</i>].caul.pElems[<i>list_specifier</i>]

where <i>n</i> is the index number of the property that is inspected and <i>list_specifier</i> is one of the following:

<table class="clsStd">
<tr>
<th>Range Specifier</th>
<th>Meaning</th>
</tr>
<tr>
<td>WIA_LIST_COUNT</td>
<td>Total number of list elements excluding the nominal value.</td>
</tr>
<tr>
<td>WIA_LIST_NOM</td>
<td>Nominal value for the property.</td>
</tr>
<tr>
<td>WIA_LIST_VALUES</td>
<td>The index number of the first value.</td>
</tr>
</table>
 

Programs also use the <i>ppvValidValues</i> parameter to retrieve valid flag values. For instance, if the property flags are specified as VT_UI4, valid flag values can be determined through the structure member 

rgpropspec[<i>n</i>].caul.pElems[<i>flag_specifier</i>]

where <i>n</i> is the index number of the property that is inspected, and <i>flag_specifier </i> is one of the following:

<table class="clsStd">
<tr>
<th>Range Specifier</th>
<th>Meaning</th>
</tr>
<tr>
<td>WIA_FLAG_NOM</td>
<td>The nominal value for the property.</td>
</tr>
<tr>
<td>WIA_FLAG_NUM_ELEMS</td>
<td>Total number of list elements excluding the nominal value.</td>
</tr>
<tr>
<td>WIA_FLAG_VALUES</td>
<td>All values with all valid flag bits set.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/propidl/nn-propidl-ipropertystorage">IPropertyStorage</a>



<a href="/windows/desktop/api/wia_xp/nn-wia_xp-iwiapropertystorage">IWiaPropertyStorage</a>