---
UID: NN:icontact.IContactProperties
title: IContactProperties (icontact.h)
description: Do not use. Used to retrieve, set, create, and remove properties on an IContact. Property names and extension mechanisms are described in icontactproperties.h.helpviewer_keywords: ["IContactProperties","IContactProperties interface [Windows Contacts]","IContactProperties interface [Windows Contacts]","described","_wincontacts_IContactProperties","icontact/IContactProperties","wincontacts._wincontacts_IContactProperties"]
old-location: wincontacts\_wincontacts_IContactProperties.htm
tech.root: wincontacts
ms.assetid: c9c0d73d-4c39-4f7c-9bc6-46d764f157bd
ms.date: 12/05/2018
ms.keywords: IContactProperties, IContactProperties interface [Windows Contacts], IContactProperties interface [Windows Contacts],described, _wincontacts_IContactProperties, icontact/IContactProperties, wincontacts._wincontacts_IContactProperties
f1_keywords:
- icontact/IContactProperties
dev_langs:
- c++
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
req.lib: 
req.dll: Wab32.dll (Version 6.0 or later)
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wab32.dll
api_name:
- IContactProperties
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IContactProperties interface


## -description


Do not use. Used to retrieve, set, create, and remove properties on an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nn-icontact-icontact">IContact</a>. 
		Property names and extension mechanisms are described in icontactproperties.h. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContactProperties</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IContactProperties</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-createarraynode">CreateArrayNode</a>
</td>
<td align="left" width="63%">
Creates a new array node in a multi-value property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-deletearraynode">DeleteArrayNode</a>
</td>
<td align="left" width="63%">
Deletes the data at a specified array entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-deletelabels">DeleteLabels</a>
</td>
<td align="left" width="63%">
Deletes the labels at a specified array entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-deleteproperty">DeleteProperty</a>
</td>
<td align="left" width="63%">
Deletes the value at a specified property. Property modification 
		and version data can still be enumerated with <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactpropertycollection">IContactPropertyCollection</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-getbinary">GetBinary</a>
</td>
<td align="left" width="63%">
Retrieves the binary data of a property using an <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-getdate">GetDate</a>
</td>
<td align="left" width="63%">
Retrieves the date and time value at a specified property into a caller's 
    <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a> structure. All times are stored 
    and returned as UTC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-getlabels">GetLabels</a>
</td>
<td align="left" width="63%">
Retrieves the labels for a specified array element name. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-getpropertycollection">GetPropertyCollection</a>
</td>
<td align="left" width="63%">
Returns an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nn-icontact-icontactpropertycollection">IContactPropertyCollection</a> for the current contact. 
		Optionally, filters the <b>IContactPropertyCollection</b> to enumerate only some values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-getstring">GetString</a>
</td>
<td align="left" width="63%">
Retrieves the string value at a specified property into a caller-allocated buffer. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-setbinary">SetBinary</a>
</td>
<td align="left" width="63%">
Sets the binary data at a specified property to the contents of a specified <a href="https://docs.microsoft.com/windows/desktop/api/objidl/nn-objidl-istream">IStream interface [Structured Storage]</a>, 
		which contains a null-terminated string (as MIME type) data. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-setdate">SetDate</a>
</td>
<td align="left" width="63%">
Sets the date and time value at a specified property to a given 
    <a href="https://docs.microsoft.com/windows/desktop/api/minwinbase/ns-minwinbase-filetime">FILETIME</a>. All times are stored and returned as UTC.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-setlabels">SetLabels</a>
</td>
<td align="left" width="63%">
Appends the set of labels passed in to the specified property's label set. 
		Note: This method does not check for duplicate labels.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/icontact/nf-icontact-icontactproperties-setstring">SetString</a>
</td>
<td align="left" width="63%">
Sets the string value of a specified property to that of a specified null-terminated string. 

</td>
</tr>
</table> 

