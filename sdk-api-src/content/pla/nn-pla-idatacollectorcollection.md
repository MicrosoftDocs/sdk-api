---
UID: NN:pla.IDataCollectorCollection
title: IDataCollectorCollection
author: windows-sdk-content
description: Manages a collection of DataCollector objects.To get this interface, access the IDataCollectorSet::DataCollectors property.
old-location: pla\idatacollectorcollection.htm
tech.root: pla
ms.assetid: 6b47fb9d-6ca4-4e6b-b117-027ef1e963ac
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollectorCollection, IDataCollectorCollection interface [PLA], IDataCollectorCollection interface [PLA],described, base.idatacollectorcollection, pla.idatacollectorcollection, pla/IDataCollectorCollection
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
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorCollection interface


## -description


Manages a collection of <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">DataCollector</a> objects.

To get this interface, access the <a href="https://msdn.microsoft.com/1bcfc15e-bc20-4dfa-a934-d0100b8db23f">IDataCollectorSet::DataCollectors</a> property.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollectorCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IDataCollectorCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDataCollectorCollection</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6302e144-74ef-4251-a857-d3e066c9763d">Add</a>
</td>
<td align="left" width="63%">
Adds a data collector to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e7482bc4-18a4-4267-9ceb-1552dd71391c">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more data collectors to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/be0840dc-e19a-454e-bbea-6968c7284cc8">Clear</a>
</td>
<td align="left" width="63%">
Removes all data collectors from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">CreateDataCollector</a>
</td>
<td align="left" width="63%">
Creates a data collector of the specified type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">CreateDataCollectorFromXml</a>
</td>
<td align="left" width="63%">
Creates a data collector using the specified XML.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f5a6d20-d65a-477b-8886-8536315bc36e">Remove</a>
</td>
<td align="left" width="63%">
Removes a data collector from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollectorCollection</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/05b97d37-9ccc-4856-a71a-77dd99eab8c2">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f18f5b40-35bb-472b-bd42-04b0a018dbf9">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of data collectors in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ab77b1ad-e09f-40fb-b285-d8a82b4b3528">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested data collector from the collection.

</td>
</tr>
</table> 

