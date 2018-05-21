---
UID: NN:comadmin.ICatalogCollection
title: ICatalogCollection
author: windows-driver-content
description: Represents any collection in the COM+ catalog. ICatalogCollection enables you to enumerate, add, remove, and retrieve items in a collection and to access related collections.
old-location: cos\icatalogcollection.htm
old-project: cossdk
ms.assetid: 7c24ead4-d69f-467d-b3d8-a81adbc49a7b
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ICatalogCollection, ICatalogCollection interface [COM+], ICatalogCollection interface [COM+],described, _cos_ICatalogCollection_Interface, comadmin/ICatalogCollection, cos.icatalogcollection
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: COMAdminTxIsolationLevelOptions
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	ComAdmin.h
api_name:
-	ICatalogCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# ICatalogCollection interface


## -description


Represents any collection in the COM+ catalog. <b>ICatalogCollection</b> enables you to enumerate, add, remove, and retrieve items in a collection and to access related collections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICatalogCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection, giving it the high index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4198f456-97fa-45b2-aa79-29ac506a8618">GetCollection</a>
</td>
<td align="left" width="63%">
Retrieves a collection from the COM+ catalog that is related to the current collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bac2153d-253b-4be1-be14-2c1207799ada">GetUtilInterface</a>
</td>
<td align="left" width="63%">
Retrieves the utility interface for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/817f203c-ddc6-47bd-a946-2393067eca44">Populate</a>
</td>
<td align="left" width="63%">
Populates the collection with data for all items contained in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/57329c32-2852-47ff-bf8c-dbb63f69841f">PopulateByKey</a>
</td>
<td align="left" width="63%">
Populates a selected list of items in the collection from the COM+ catalog, based on the specified keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30e4bb16-f99f-4541-a70a-64eb285df7b6">PopulateByQuery</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection, given its index, and re-indexes the items with higher index values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ae984eee-4a8d-48e5-839c-fa115fd4aeea">SaveChanges</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/6a8b0773-5ea7-4ad2-a520-ec9ea74a8755">AddEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/library/windows/hardware/dn938485">Add</a> method is enabled for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


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

<a href="https://msdn.microsoft.com/846f4966-ff58-46b5-a56a-dc14f64fcae7">DataStoreMajorVersion</a>


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

<a href="https://msdn.microsoft.com/29380ed1-835e-4ac9-afeb-869acd748ebc">DataStoreMinorVersion</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


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

<a href="https://msdn.microsoft.com/eda0812f-a0e4-4239-87b5-c252e9e3492c">RemoveEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a> method is enabled for the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2530e44f-c428-4baa-88e1-8d01eaf234cc">COMAdminCatalogCollection</a>
 

 

