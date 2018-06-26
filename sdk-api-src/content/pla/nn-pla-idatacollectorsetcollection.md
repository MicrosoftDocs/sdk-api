---
UID: NN:pla.IDataCollectorSetCollection
title: IDataCollectorSetCollection
author: windows-sdk-content
description: Manages a collection of DataCollectorSet objects.To get this interface, call the CoCreateInstance function, passing __uuidof(DataCollectorSetCollection) as the class identifier and __uuidof(IDataCollectorSetCollection) as the interface identifier.Then, to populate the collection, call the IDataCollectorSetCollection::GetDataCollectorSets method.
old-location: pla\idatacollectorsetcollection.htm
old-project: PLA
ms.assetid: 5f4cc411-1efb-4f70-a677-3c20d95f0c53
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDataCollectorSetCollection, IDataCollectorSetCollection interface [PLA], IDataCollectorSetCollection interface [PLA],described, base.idatacollectorsetcollection, pla.idatacollectorsetcollection, pla/IDataCollectorSetCollection
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSetCollection
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: ADAM
---

# IDataCollectorSetCollection interface


## -description


Manages a collection of <a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">DataCollectorSet</a> objects.

To get this interface, call the <b>CoCreateInstance</b> function, passing __uuidof(DataCollectorSetCollection) as the class identifier and __uuidof(<b>IDataCollectorSetCollection</b>) as the interface identifier.

Then, to populate the collection, call the <a href="https://msdn.microsoft.com/190c96ad-6193-4f74-906f-180575e6e418">IDataCollectorSetCollection::GetDataCollectorSets</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollectorSetCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IDataCollectorSetCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDataCollectorSetCollection</b> interface has these methods.
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
Adds a data collector set to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/52a7d9ba-9bff-428e-a43c-cc354157fd24">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more data collector sets to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all data collector sets from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/190c96ad-6193-4f74-906f-180575e6e418">GetDataCollectorSets</a>
</td>
<td align="left" width="63%">
Populates the data collector set collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes a data collector set from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollectorSetCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439300">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of data collector sets in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested data collector set from the collection.

</td>
</tr>
</table> 


## -remarks



To create the object from a script, use the Pla.DataCollectorSetCollection program identifier.



