---
UID: NN:wuapi.IStringCollection
title: IStringCollection (wuapi.h)
description: Represents an ordered list of strings.
old-location: wua\istringcollection.htm
tech.root: Wua_Sdk
ms.assetid: 3aaab669-1f80-41ee-8c29-6da613ebccff
ms.date: 12/05/2018
ms.keywords: IStringCollection, IStringCollection interface [Windows Update Agent], IStringCollection interface [Windows Update Agent],described, wua.istringcollection, wuapi/IStringCollection
f1_keywords:
- wuapi/IStringCollection
dev_langs:
- c++
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Wuapi.dll
api_name:
- IStringCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStringCollection interface


## -description


Represents an ordered list of strings.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IStringCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IStringCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all the elements from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-copy">Copy</a>
</td>
<td align="left" width="63%">
Creates a deep read/write copy of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-insert">Insert</a>
</td>
<td align="left" width="63%">
Inserts an item into the collection at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-removeat">RemoveAt</a>
</td>
<td align="left" width="63%">
Removes the item at the specified index from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IStringCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets an <b>IEnumVARIANT</b> interface that can be used to enumerate the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets the number of elements in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-get_item">Item</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Gets or sets a string in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/wuapi/nf-wuapi-istringcollection-get_readonly">ReadOnly</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Gets a Boolean value that indicates whether the collection is read-only.

</td>
</tr>
</table> 


## -remarks



This interface can be instantiated by using the StringCollection coclass. Use the Microsoft.Update.StringColl program identifier to create the object.



