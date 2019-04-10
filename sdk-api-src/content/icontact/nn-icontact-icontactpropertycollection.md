---
UID: NN:icontact.IContactPropertyCollection
title: IContactPropertyCollection (icontact.h)
author: windows-sdk-content
description: Do not use. Used to filter contact data, based on a label or property set. Enumerates contact properties exposed with an IContactProperties object. For each property, the name, type, version, and modification date can be retrieved.
old-location: wincontacts\_wincontacts_IContactPropertyCollection.htm
tech.root: wincontacts
ms.assetid: dec9430d-2174-42fe-85c1-16fa7e7adc0c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IContactPropertyCollection, IContactPropertyCollection interface [Windows Contacts], IContactPropertyCollection interface [Windows Contacts],described, _wincontacts_IContactPropertyCollection, icontact/IContactPropertyCollection, wincontacts._wincontacts_IContactPropertyCollection
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
 - IContactPropertyCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IContactPropertyCollection interface


## -description


Do not use. Used to filter contact data, based on a label or property set. Enumerates contact properties 
		exposed with an <a href="https://msdn.microsoft.com/c9c0d73d-4c39-4f7c-9bc6-46d764f157bd">IContactProperties</a> object. For each property, 
		the name, type, version, and modification date can be retrieved.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContactPropertyCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IContactPropertyCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContactPropertyCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bfd860d6-cd67-4f97-afc4-1e2e7c8f57ca">GetPropertyArrayElementID</a>
</td>
<td align="left" width="63%">
Retrieves the unique ID for a given element in a property array.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7ad95916-4e21-4607-b27d-584a931f9201">GetPropertyModificationDate</a>
</td>
<td align="left" width="63%">
Retrieves the last modification date for the current property in the enumeration. 
		If not modified, contact creation date is returned.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8fa7fb24-2648-4f7b-b37c-d42b2966a959">GetPropertyName</a>
</td>
<td align="left" width="63%">
Retrieves the name for the current property in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/11977b0c-332a-415a-986f-7fb08246413f">GetPropertyType</a>
</td>
<td align="left" width="63%">
Retrieves the type for the current property in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff10129e-45cb-41a4-8800-22b33a238b65">GetPropertyVersion</a>
</td>
<td align="left" width="63%">
Retrieves the version number for the current property in the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6e8abad-796d-4ded-be23-45ca107915f1">Next</a>
</td>
<td align="left" width="63%">
Moves to the next property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cef73e3c-56be-44b8-b05b-3c2081b71591">Reset</a>
</td>
<td align="left" width="63%">
Resets enumeration of properties.

</td>
</tr>
</table> 


## -remarks



<div class="alert"><b>Note</b>  Changing the <a href="https://msdn.microsoft.com/c9c0d73d-4c39-4f7c-9bc6-46d764f157bd">IContactProperties</a> properties object 
		while enumerating properties with this interface results in undefined behavior.</div>
<div> </div>


