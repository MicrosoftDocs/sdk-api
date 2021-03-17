---
UID: NF:msinkaut.IInkExtendedProperties.Remove
title: IInkExtendedProperties::Remove (msinkaut.h)
description: Removes the IInkExtendedProperty object from the IInkExtendedProperties collection.
helpviewer_keywords: ["2211a462-df26-4168-b89c-9607683defdb","IInkExtendedProperties interface [Tablet PC]","Remove method","IInkExtendedProperties.Remove","IInkExtendedProperties::Remove","Remove","Remove method [Tablet PC]","Remove method [Tablet PC]","IInkExtendedProperties interface","msinkaut/IInkExtendedProperties::Remove","tablet.iinkextendedproperties_remove"]
old-location: tablet\iinkextendedproperties_remove.htm
tech.root: tablet
ms.assetid: 2211a462-df26-4168-b89c-9607683defdb
ms.date: 12/05/2018
ms.keywords: 2211a462-df26-4168-b89c-9607683defdb, IInkExtendedProperties interface [Tablet PC],Remove method, IInkExtendedProperties.Remove, IInkExtendedProperties::Remove, Remove, Remove method [Tablet PC], Remove method [Tablet PC],IInkExtendedProperties interface, msinkaut/IInkExtendedProperties::Remove, tablet.iinkextendedproperties_remove
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkExtendedProperties::Remove
 - msinkaut/IInkExtendedProperties::Remove
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkExtendedProperties.Remove
---

# IInkExtendedProperties::Remove


## -description

Removes the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty</a> object from the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties</a> collection.

## -parameters

### -param Identifier [in]

The identifier of the <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty</a> object to remove from the collection. The identifier can be a globally unique identifier (GUID), an index, or an extended property object.

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -returns

This method can return one of these values.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TPC_E_INVALID_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
Property could not be found (invalid GUID or index).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred inside the method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid display handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>

## -remarks

This method removes only the extended property from a snapshot of, or reference to, the ink data and does not remove the actual ink data.

The <i>Identifier</i> parameter can be a BSTR, a LONG, or an <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>. Use a BSTR for the GUID of the property, a LONG for the index of the property, and an <b>IDispatch</b> for a reference to a specific property. To specify the GUID of the property when you are using late binding, such as when you use a scripting language, you must pass in the argument as a STRING literal and not use a variable.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties Interface</a>