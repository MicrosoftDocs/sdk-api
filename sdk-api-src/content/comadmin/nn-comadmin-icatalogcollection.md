---
UID: NN:comadmin.ICatalogCollection
title: ICatalogCollection
author: windows-sdk-content
description: Represents any collection in the COM+ catalog. ICatalogCollection enables you to enumerate, add, remove, and retrieve items in a collection and to access related collections.
old-location: cos\icatalogcollection.htm
tech.root: cossdk
ms.assetid: 7c24ead4-d69f-467d-b3d8-a81adbc49a7b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: ICatalogCollection, ICatalogCollection interface [COM+], ICatalogCollection interface [COM+],described, _cos_ICatalogCollection_Interface, comadmin/ICatalogCollection, cos.icatalogcollection
ms.prod: windows
ms.technology: windows-sdk
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICatalogCollection interface


## -description


Represents any collection in the COM+ catalog. <b>ICatalogCollection</b> enables you to enumerate, add, remove, and retrieve items in a collection and to access related collections.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICatalogCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICatalogCollection</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/ms678897(v=VS.85).aspx">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection, giving it the high index value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms680613(v=VS.85).aspx">GetCollection</a>
</td>
<td align="left" width="63%">
Retrieves a collection from the COM+ catalog that is related to the current collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms686079(v=VS.85).aspx">GetUtilInterface</a>
</td>
<td align="left" width="63%">
Retrieves the utility interface for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms683485(v=VS.85).aspx">Populate</a>
</td>
<td align="left" width="63%">
Populates the collection with data for all items contained in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms681322(v=VS.85).aspx">PopulateByKey</a>
</td>
<td align="left" width="63%">
Populates a selected list of items in the collection from the COM+ catalog, based on the specified keys.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms679557(v=VS.85).aspx">PopulateByQuery</a>
</td>
<td align="left" width="63%">
Reserved for future use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms684329(v=VS.85).aspx">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection, given its index, and re-indexes the items with higher index values.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms685204(v=VS.85).aspx">SaveChanges</a>
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

<a href="https://msdn.microsoft.com/en-us/library/ms683508(v=VS.85).aspx">_NewEnum</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms682213(v=VS.85).aspx">AddEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/en-us/library/ms678897(v=VS.85).aspx">Add</a> method is enabled for the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/ms686117(v=VS.85).aspx">Count</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms683563(v=VS.85).aspx">DataStoreMajorVersion</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms679496(v=VS.85).aspx">DataStoreMinorVersion</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms681193(v=VS.85).aspx">Item</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms678913(v=VS.85).aspx">Name</a>


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

<a href="https://msdn.microsoft.com/en-us/library/ms687739(v=VS.85).aspx">RemoveEnabled</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Indicates whether the <a href="https://msdn.microsoft.com/en-us/library/ms684329(v=VS.85).aspx">Remove</a> method is enabled for the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/2530e44f-c428-4baa-88e1-8d01eaf234cc">COMAdminCatalogCollection</a>
 

 

