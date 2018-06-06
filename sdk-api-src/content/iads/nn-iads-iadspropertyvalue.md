---
UID: NN:iads.IADsPropertyValue
title: IADsPropertyValue
author: windows-sdk-content
description: Used to represent the value of an IADsPropertyEntry object in a predefined data type.
old-location: adsi\iadspropertyvalue.htm
old-project: ADSI
ms.assetid: 7cad4d04-80d4-4f9a-95b7-2f1809ddb8fb
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IADsPropertyValue, IADsPropertyValue interface [ADSI], IADsPropertyValue interface [ADSI],described, PropertyValue, _ds_iadspropertyvalue, adsi.iadspropertyvalue, iads/IADsPropertyValue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
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
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsPropertyValue interface


## -description


The <b>IADsPropertyValue</b> interface is used to represent the value of an <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> object in a predefined data type. This interface exposes several properties for obtaining data values in the corresponding data format.

The <a href="https://msdn.microsoft.com/73b0f6d4-55db-46cf-a781-e10bc4fcf2db">IADsPropertyEntry.Values</a> property contains an array of <b>IADsPropertyValue</b> objects. Each of the <b>IADsPropertyValue</b> objects contains a single value of the <a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a> object. For more information and a code example for creating entirely new property entries and values, see <a href="https://msdn.microsoft.com/16af5cbf-3b87-467e-8e72-0110bcf95295">IADsPropertyList.PutPropertyItem</a>.

When obtaining values in a format not provided by one of the properties of this interface, use the  <a href="https://msdn.microsoft.com/57a3b413-f658-4793-abad-358455b5b9f4">IADsPropertyValue2</a> interface.

Before calling the methods of this interfaces, call  <a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs.GetInfo</a> or  <a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs.GetInfoEx</a> explicitly to load the assigned values of the object into the cache, if the cache has not been initialized. After modifying the properties of this interface, call  <a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs.SetInfo</a> to save the changes to the persistent store of the underlying directory.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPropertyValue</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IADsPropertyValue</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">ADsType</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">Boolean</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">CaseExactString</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">CaseIgnoreString</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">DNString</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">Integer</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">LargeInteger</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">NumericString</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">OctetString</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">PrintableString</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">SecurityDescriptor</a>


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

<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">UTCTime</a>


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




<a href="https://msdn.microsoft.com/73ceaeb1-9a6b-449a-9851-3756736dbad7">IADs::GetInfo</a>



<a href="https://msdn.microsoft.com/306ab953-890a-4ec9-8ec2-bea73888ea20">IADs::GetInfoEx</a>



<a href="https://msdn.microsoft.com/e7ff6acd-b7c4-463d-a34f-fd793067c63a">IADs::SetInfo</a>



<a href="https://msdn.microsoft.com/6c398d05-ac12-4c9a-b61a-70cd795c991f">IADsPropertyEntry</a>



<a href="https://msdn.microsoft.com/1039d4a9-bef8-457d-9a32-3743c14adef1">IADsPropertyValue Property Methods</a>



<a href="https://msdn.microsoft.com/57a3b413-f658-4793-abad-358455b5b9f4">IADsPropertyValue2</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

