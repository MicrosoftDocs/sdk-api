---
UID: NN:comadmin.ICatalogCollection
title: ICatalogCollection (comadmin.h)
description: Represents any collection in the COM+ catalog. ICatalogCollection enables you to enumerate, add, remove, and retrieve items in a collection and to access related collections.
helpviewer_keywords: ["ICatalogCollection","ICatalogCollection interface [COM+]","ICatalogCollection interface [COM+]","described","_cos_ICatalogCollection_Interface","comadmin/ICatalogCollection","cos.icatalogcollection"]
old-location: cos\icatalogcollection.htm
tech.root: cossdk
ms.assetid: 7c24ead4-d69f-467d-b3d8-a81adbc49a7b
ms.date: 12/05/2018
ms.keywords: ICatalogCollection, ICatalogCollection interface [COM+], ICatalogCollection interface [COM+],described, _cos_ICatalogCollection_Interface, comadmin/ICatalogCollection, cos.icatalogcollection
f1_keywords:
- comadmin/ICatalogCollection
dev_langs:
- c++
req.header: comadmin.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComAdmin.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- ComAdmin.h
api_name:
- ICatalogCollection
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICatalogCollection interface


## -description


Represents any collection in the COM+ catalog. <b>ICatalogCollection</b> enables you to enumerate, add, remove, and retrieve items in a collection and to access related collections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICatalogCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICatalogCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection, giving it the high index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-getcollection">GetCollection</a>
</td>
<td align="left" width="63%">
Retrieves a collection from the COM+ catalog that is related to the current collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-getutilinterface">GetUtilInterface</a>
</td>
<td align="left" width="63%">
Retrieves the utility interface for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-populate">Populate</a>
</td>
<td align="left" width="63%">
Populates the collection with data for all items contained in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-populatebykey">PopulateByKey</a>
</td>
<td align="left" width="63%">
Populates a selected list of items in the collection from the COM+ catalog, based on the specified keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-populatebyquery">PopulateByQuery</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-remove">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection, given its index, and re-indexes the items with higher index values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-savechanges">SaveChanges</a>
</td>
<td align="left" width="63%">
Saves all pending changes made to the collection and the items it contains to the COM+ catalog data store.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
An enumerator that can be used to iterate through the collection objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_addenabled">AddEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-add">Add</a> method is enabled for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_count">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_datastoremajorversion">DataStoreMajorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The major version number of the catalog data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_datastoreminorversion">DataStoreMinorVersion</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The minor version number of the catalog data store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_item">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The item that correspond to the specified index.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_name">Name</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
The name of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-get_removeenabled">RemoveEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://docs.microsoft.com/windows/desktop/api/comadmin/nf-comadmin-icatalogcollection-remove">Remove</a> method is enabled for the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/cossdk/comadmincatalogcollection">COMAdminCatalogCollection</a>
 

 

