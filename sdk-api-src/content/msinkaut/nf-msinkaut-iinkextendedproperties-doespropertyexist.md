---
UID: NF:msinkaut.IInkExtendedProperties.DoesPropertyExist
title: IInkExtendedProperties::DoesPropertyExist (msinkaut.h)
description: Retrieves a value that indicates whether an IInkExtendedProperty object exists within an IInkExtendedProperties collection.
helpviewer_keywords: ["285d6ce3-f7f9-48b0-aaa2-d9ff8db732eb","DoesPropertyExist","DoesPropertyExist method [Tablet PC]","DoesPropertyExist method [Tablet PC]","IInkExtendedProperties interface","IInkExtendedProperties interface [Tablet PC]","DoesPropertyExist method","IInkExtendedProperties.DoesPropertyExist","IInkExtendedProperties::DoesPropertyExist","msinkaut/IInkExtendedProperties::DoesPropertyExist","tablet.iinkextendedproperties_doespropertyexist"]
old-location: tablet\iinkextendedproperties_doespropertyexist.htm
tech.root: tablet
ms.assetid: 285d6ce3-f7f9-48b0-aaa2-d9ff8db732eb
ms.date: 12/05/2018
ms.keywords: 285d6ce3-f7f9-48b0-aaa2-d9ff8db732eb, DoesPropertyExist, DoesPropertyExist method [Tablet PC], DoesPropertyExist method [Tablet PC],IInkExtendedProperties interface, IInkExtendedProperties interface [Tablet PC],DoesPropertyExist method, IInkExtendedProperties.DoesPropertyExist, IInkExtendedProperties::DoesPropertyExist, msinkaut/IInkExtendedProperties::DoesPropertyExist, tablet.iinkextendedproperties_doespropertyexist
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
 - IInkExtendedProperties::DoesPropertyExist
 - msinkaut/IInkExtendedProperties::DoesPropertyExist
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
 - IInkExtendedProperties.DoesPropertyExist
---

# IInkExtendedProperties::DoesPropertyExist


## -description

Retrieves a value that indicates whether an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperty">IInkExtendedProperty</a> object exists within an <a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties</a> collection.

## -parameters

### -param Guid [in]

Specifies the globally unique identifier (GUID) of the property to be checked.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param DoesPropertyExist [out, retval]

When this method returns, contains <b>VARIANT_TRUE</b> if the property exists within the collection; otherwise, <b>VARIANT_FALSE</b>.

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
<dt><b>TPC_E_INVALID_STROKE</b></dt>
</dl>
</td>
<td width="60%">
The stroke is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkextendedproperties">IInkExtendedProperties Interface</a>