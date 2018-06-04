---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# ITraceDataProviderCollection interface


## -description


Manages a collection of <a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">TraceDataProvider</a> objects.

To get this interface, access the <a href="https://msdn.microsoft.com/7a2006e8-3c4c-4441-8c9e-be9ce584dd63">ITraceDataCollector::TraceDataProviders</a> property.

You can also call the <b>CoCreateInstance</b> function to create a new instance of the <b>TraceDataProviderCollection</b> object. Pass __uuidof(TraceDataProviderCollection) as the class identifier and __uuidof(<b>ITraceDataProviderCollection</b>) as the interface identifier.

To populate the collection with registered providers, call the <a href="https://msdn.microsoft.com/ff35087e-be55-42e8-96e9-c923d06248d8">ITraceDataProviderCollection::GetTraceDataProviders</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceDataProviderCollection</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ITraceDataProviderCollection</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITraceDataProviderCollection</b> interface has these methods.
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
Adds a trace provider to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/235c390a-c31c-4b31-bece-3ea7ac345391">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more trace providers to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406339">Clear</a>
</td>
<td align="left" width="63%">
Removes all trace providers from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/234de4d8-896f-462d-8785-8b768697bf2e">CreateTraceDataProvider</a>
</td>
<td align="left" width="63%">
Creates a trace data provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ff35087e-be55-42e8-96e9-c923d06248d8">GetTraceDataProviders</a>
</td>
<td align="left" width="63%">
Populates the collection with registered trace providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bc8b6aeb-7239-4bce-8616-62f87b84ae6c">GetTraceDataProvidersByProcess</a>
</td>
<td align="left" width="63%">
Populates the collection with the list of providers that have been registered by the specified process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439492">Remove</a>
</td>
<td align="left" width="63%">
Removes a trace provider from the collection.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceDataProviderCollection</b> interface has these properties.
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
Retrieves the number of trace providers in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh451057">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested trace provider from the collection.

</td>
</tr>
</table> 


## -remarks



To create the object from a script, use the Pla.TraceDataProviderCollection program identifier.



