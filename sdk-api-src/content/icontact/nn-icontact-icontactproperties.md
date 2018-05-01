---
UID: NN:icontact.IContactProperties
title: IContactProperties
author: windows-driver-content
description: Do not use. Used to retrieve, set, create, and remove properties on an IContact. Property names and extension mechanisms are described in icontactproperties.h.
old-location: wincontacts\_wincontacts_IContactProperties.htm
old-project: wincontacts
ms.assetid: c9c0d73d-4c39-4f7c-9bc6-46d764f157bd
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IContactProperties, IContactProperties interface [Windows Contacts], IContactProperties interface [Windows Contacts], described, _wincontacts_IContactProperties, icontact/IContactProperties, wincontacts._wincontacts_IContactProperties
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: icontact.h
req.include-header: Contact.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Icontact.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NET_FW_SERVICE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wab32.dll
api_name:
-	IContactProperties
product: Windows
targetos: Windows
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
req.product: GDI+ 1.1
---

# IContactProperties interface


## -description


Do not use. Used to retrieve, set, create, and remove properties on an <a href="https://msdn.microsoft.com/9dc97b84-ede9-4ec1-939a-2b13e0d68486">IContact</a>. 
		Property names and extension mechanisms are described in icontactproperties.h. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContactProperties</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContactProperties</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContactProperties</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/422b9991-c8ac-4e8b-9432-1ccba02f7cfd">CreateArrayNode</a>
</td>
<td align="left" width="63%">
Creates a new array node in a multi-value property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a26dc392-1dd7-4dba-9802-b45c01d97493">DeleteArrayNode</a>
</td>
<td align="left" width="63%">
Deletes the data at a specified array entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0925bed9-26ef-46e6-9087-0e1a1e57349d">DeleteLabels</a>
</td>
<td align="left" width="63%">
Deletes the labels at a specified array entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74ed72da-e82c-4257-9d16-c5204a88c9bf">DeleteProperty</a>
</td>
<td align="left" width="63%">
Deletes the value at a specified property. Property modification 
		and version data can still be enumerated with <a href="https://msdn.microsoft.com/dec9430d-2174-42fe-85c1-16fa7e7adc0c">IContactPropertyCollection</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1a62c5d3-7052-4c10-90e7-25f616ac36b8">GetBinary</a>
</td>
<td align="left" width="63%">
Retrieves the binary data of a property using an <a href="_stg_istream">IStream interface [Structured Storage]</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0ee9a870-ad51-4528-b830-bee72586b936">GetDate</a>
</td>
<td align="left" width="63%">
Retrieves the date and time value at a specified property into a caller's 
    <a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a> structure. All times are stored 
    and returned as UTC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c639a30b-3778-4ed9-b175-60b4a7ba9748">GetLabels</a>
</td>
<td align="left" width="63%">
Retrieves the labels for a specified array element name. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12ef5ff0-ac87-4475-86b3-31a6379ffb4e">GetPropertyCollection</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://msdn.microsoft.com/dec9430d-2174-42fe-85c1-16fa7e7adc0c">IContactPropertyCollection</a> for the current contact. 
		Optionally, filters the <b>IContactPropertyCollection</b> to enumerate only some values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983419">GetString</a>
</td>
<td align="left" width="63%">
Retrieves the string value at a specified property into a caller-allocated buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/432c2417-e762-47ff-b2ce-a244120f0545">SetBinary</a>
</td>
<td align="left" width="63%">
Sets the binary data at a specified property to the contents of a specified <a href="_stg_istream">IStream interface [Structured Storage]</a>, 
		which contains a null-terminated string (as MIME type) data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bbe0a788-7291-48f7-a36a-88e5b6b971dc">SetDate</a>
</td>
<td align="left" width="63%">
Sets the date and time value at a specified property to a given 
    <a href="6ca5e0f1-24f8-4087-bf13-7a417bed3ccd">FILETIME</a>. All times are stored and returned as UTC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/884d4edf-e001-4a1d-9ee4-7f8733aba343">SetLabels</a>
</td>
<td align="left" width="63%">
Appends the set of labels passed in to the specified property's label set. 
		Note: This method does not check for duplicate labels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/jj983427">SetString</a>
</td>
<td align="left" width="63%">
Sets the string value of a specified property to that of a specified null-terminated string. 

</td>
</tr>
</table> 

