---
UID: NN:iads.IADsPropertyList
title: IADsPropertyList (iads.h)
author: windows-sdk-content
description: The IADsPropertyList interface is used to modify, read, and update a list of property entries in the property cache of an object.
old-location: adsi\iadspropertylist.htm
tech.root: adsi
ms.assetid: 70e9ce0e-ae83-43b7-8b84-99d5e1f8a8d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IADsPropertyList, IADsPropertyList interface [ADSI], IADsPropertyList interface [ADSI],described, _ds_iadspropertylist, adsi.iadspropertylist, iads/IADsPropertyList
ms.topic: interface
f1_keywords: 
 - "iads/IADsPropertyList"
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
 - IADsPropertyList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IADsPropertyList interface


## -description


The <b>IADsPropertyList</b> interface is used to modify, read, and update a list of property entries in the property cache of an object. It serves to enumerate, modify, and purge the contained property entries. Use the enumeration method of this interface to identify initialized properties. This is different from using the schema to determine all possible attributes that an ADSI object can have and which properties have been set.
   

Call the methods of the <b>IADsPropertyList</b> interface to examine and manipulate the property list on the client. Before calling the methods of this interface, you must call  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a> explicitly to load the assigned property values of the object into the cache. After calling the methods of this interface, you must call  <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a> to save the changes in the persistent store of the underlying directory.

To obtain the property list of an ADSI object, bind to its <b>IADsPropertyList</b> interface. You must call the <a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">GetInfo</a> method before calling other methods of property list object, if the property cache has not been initialized.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPropertyList</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IADsPropertyList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IADsPropertyList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-getpropertyitem">GetPropertyItem</a>
</td>
<td align="left" width="63%">
Gets the value of a named property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-item">Item</a>
</td>
<td align="left" width="63%">
Gets a property that is specified by name or by index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-next">Next</a>
</td>
<td align="left" width="63%">
Gets the next item in the property list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-purgepropertylist">PurgePropertyList</a>
</td>
<td align="left" width="63%">
Deletes all properties from the list and, therefore, releases the property caches as well.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-putpropertyitem">PutPropertyItem</a>
</td>
<td align="left" width="63%">
Puts the value of a named property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-reset">Reset</a>
</td>
<td align="left" width="63%">
Moves back to the start of the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-resetpropertyitem">ResetPropertyItem</a>
</td>
<td align="left" width="63%">
Resets the value of a named property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iadspropertylist-skip">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the property list.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IADsPropertyList</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertylist-property-methods">PropertyCount</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of properties in the property list.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfo">IADs::GetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-getinfoex">IADs::GetInfoEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/iads/nf-iads-iads-setinfo">IADs::SetInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/ADSI/iadspropertylist-property-methods">IADsPropertyList Property Methods</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

