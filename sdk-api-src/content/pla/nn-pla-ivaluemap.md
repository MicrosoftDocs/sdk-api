---
UID: NN:pla.IValueMap
title: IValueMap (pla.h)
author: windows-sdk-content
description: Manages a collection of name/value pairs.To get this interface, access one of the following properties or methods:IDataCollector::SetXmlIDataCollectorSet::CommitIDataCollectorSet::SetXmlITraceDataProvider::KeywordsAllITraceDataProvider::KeywordsAnyITraceDataProvider::LevelITraceDataProvider::Properties
old-location: pla\ivaluemap.htm
tech.root: PLA
ms.assetid: a7134395-91c6-4ea1-8b76-63830048289f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IValueMap, IValueMap interface [PLA], IValueMap interface [PLA],described, base.ivaluemap, pla.ivaluemap, pla/IValueMap
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
 - IValueMap
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IValueMap interface


## -description


Manages a collection of name/value pairs.

To get this interface, access one of the following properties or methods:<ul>
<li>
<a href="https://msdn.microsoft.com/12ed8697-caec-45d5-9ecf-658b3e4ca8ba">IDataCollector::SetXml</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">IDataCollectorSet::SetXml</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9ff48234-927b-4b87-a9b8-2a1047b5e3de">ITraceDataProvider::KeywordsAll</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">ITraceDataProvider::KeywordsAny</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5e9390c4-12d4-4087-b4c8-5f58c2522a93">ITraceDataProvider::Level</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1dc21423-fa55-4312-b86a-63d4f59e4cf1">ITraceDataProvider::Properties</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValueMap</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IValueMap</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IValueMap</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a6f074d-8d18-44ea-bbbc-8d3a7f6c033a">Add</a>
</td>
<td align="left" width="63%">
Adds an item to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/80893a3d-fcfc-475f-86ad-d19bb9e43ee0">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more items to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/41c80954-efc2-47ff-87e2-f33d7123cb40">Clear</a>
</td>
<td align="left" width="63%">
Removes all items from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/619b54a0-7015-4453-a09e-ac199eb1c581">CreateValueMapItem</a>
</td>
<td align="left" width="63%">
Creates a value map item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dc674243-ec0f-496f-bffb-faf4262a42c7">Remove</a>
</td>
<td align="left" width="63%">
Removes an item from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IValueMap</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1d40104c-c0a4-41d2-8427-364c37b52e02">_NewEnum</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/990b48d8-357f-4157-a3d2-1ea1c80e1887">Count</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the number of items in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/04936082-e377-46f3-b218-28a2403eee9d">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets a description of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a01f134d-9700-4826-9040-d5d6340241de">Item</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the requested item from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f344845-956e-4254-82e2-e4e00f6a371b">Value</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the value of the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/42cea1e6-c945-4bae-ac65-a052b4069e5f">ValueMapType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the type of the items in the collection.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/5fab2a62-d974-49f7-ac81-c704d9d8624c">IValueMapItem</a>
 

 

