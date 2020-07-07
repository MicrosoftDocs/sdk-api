---
UID: NN:iads.IADsPropertyValue
title: IADsPropertyValue (iads.h)
description: Used to represent the value of an IADsPropertyEntry object in a predefined data type.
helpviewer_keywords: ["IADsPropertyValue","IADsPropertyValue interface [ADSI]","IADsPropertyValue interface [ADSI]","described","PropertyValue","_ds_iadspropertyvalue","adsi.iadspropertyvalue","iads/IADsPropertyValue"]
old-location: adsi\iadspropertyvalue.htm
tech.root: adsi
ms.assetid: 7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb
ms.date: 12/05/2018
ms.keywords: IADsPropertyValue, IADsPropertyValue interface [ADSI], IADsPropertyValue interface [ADSI],described, PropertyValue, _ds_iadspropertyvalue, adsi.iadspropertyvalue, iads/IADsPropertyValue
f1_keywords:
- iads/IADsPropertyValue
dev_langs:
- c++
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Activeds.dll
api_name:
- IADsPropertyValue
- PropertyValue
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsPropertyValue interface


## -description


The <b>IADsPropertyValue</b> interface is used to represent the value of an <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> object in a predefined data type. This interface exposes several properties for obtaining data values in the corresponding data format.

The <a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyentry-property-methods">IADsPropertyEntry.Values</a> property contains an array of <b>IADsPropertyValue</b> objects. Each of the <b>IADsPropertyValue</b> objects contains a single value of the <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a> object. For more information and a code example for creating entirely new property entries and values, see <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-putpropertyitem">IADsPropertyList.PutPropertyItem</a>.

When obtaining values in a format not provided by one of the properties of this interface, use the  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a> interface.

Before calling the methods of this interfaces, call  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs.GetInfo</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs.GetInfoEx</a> explicitly to load the assigned values of the object into the cache, if the cache has not been initialized. After modifying the properties of this interface, call  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs.SetInfo</a> to save the changes to the persistent store of the underlying directory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPropertyValue</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsPropertyValue</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsPropertyValue</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertyvalue-clear">Clear</a>
</td>
<td align="left" width="63%">
Clears the current value of the PropertyValue object.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPropertyValue</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">ADsType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a property value's data type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">Boolean</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Boolean value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">CaseExactString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the value of a case-sensitive string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">CaseIgnoreString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the value of a case-insensitive string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">DNString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets an object's distinguished name (path).

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">Integer</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets an integer value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">LargeInteger</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a large-integer value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">NumericString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the value of a string consisting of numeric characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">OctetString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the value of a string of eight-bit characters.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">PrintableString</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets the value of a printable string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">SecurityDescriptor</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a security descriptor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">UTCTime</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets and sets a Coordinated Universal Time value.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyentry">IADsPropertyEntry</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertyvalue-property-methods">IADsPropertyValue Property Methods</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nn-iads-iadspropertyvalue2">IADsPropertyValue2</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

