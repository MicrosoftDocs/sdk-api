---
UID: NF:msinkaut.IInkExtendedProperties.Remove
title: IInkExtendedProperties::Remove
author: windows-sdk-content
description: Removes the IInkExtendedProperty object from the IInkExtendedProperties collection.
old-location: tablet\iinkextendedproperties_remove.htm
tech.root: tablet
ms.assetid: 2211a462-df26-4168-b89c-9607683defdb
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 2211a462-df26-4168-b89c-9607683defdb, IInkExtendedProperties interface [Tablet PC],Remove method, IInkExtendedProperties.Remove, IInkExtendedProperties::Remove, Remove, Remove method [Tablet PC], Remove method [Tablet PC],IInkExtendedProperties interface, msinkaut/IInkExtendedProperties::Remove, tablet.iinkextendedproperties_remove
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- msinkaut.h
: 
- IInkExtendedProperties.Remove
: 
---

# IInkExtendedProperties::Remove


## -description



Removes the <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> object from the <a href="https://msdn.microsoft.com/c7b7f40f-0c28-4848-83d6-d5db73eef998">IInkExtendedProperties</a> collection.




## -parameters




### -param Identifier [in]

The identifier of the <a href="https://msdn.microsoft.com/53146f37-343a-4886-a0bb-d76d50ca96ba">IInkExtendedProperty</a> object to remove from the collection. The identifier can be a globally unique identifier (GUID), an index, or an extended property object.

For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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

The <i>Identifier</i> parameter can be a BSTR, a LONG, or an <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>. Use a BSTR for the GUID of the property, a LONG for the index of the property, and an <b>IDispatch</b> for a reference to a specific property. To specify the GUID of the property when you are using late binding, such as when you use a scripting language, you must pass in the argument as a STRING literal and not use a variable.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.




## -see-also




<a href="https://msdn.microsoft.com/c7b7f40f-0c28-4848-83d6-d5db73eef998">IInkExtendedProperties Interface</a>
 

 

