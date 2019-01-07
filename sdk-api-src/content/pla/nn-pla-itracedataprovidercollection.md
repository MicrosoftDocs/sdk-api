---
UID: NN:pla.ITraceDataProviderCollection
title: ITraceDataProviderCollection
author: windows-sdk-content
description: Manages a collection of TraceDataProvider objects.To get this interface, access the ITraceDataCollector::TraceDataProviders property.You can also call the CoCreateInstance function to create a new instance of the TraceDataProviderCollection object.
old-location: pla\itracedataprovidercollection.htm
tech.root: PLA
ms.assetid: 74300222-dca4-4871-bae3-0c3182fbc539
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITraceDataProviderCollection, ITraceDataProviderCollection interface [PLA], ITraceDataProviderCollection interface [PLA],described, base.itracedataprovidercollection, pla.itracedataprovidercollection, pla/ITraceDataProviderCollection
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
 - ITraceDataProviderCollection
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceDataProviderCollection interface


## -description


Manages a collection of <a href="https://msdn.microsoft.com/bd2a49c1-8e18-4a14-a797-07f2b9c25812">TraceDataProvider</a> objects.

To get this interface, access the <a href="https://msdn.microsoft.com/7a2006e8-3c4c-4441-8c9e-be9ce584dd63">ITraceDataCollector::TraceDataProviders</a> property.

You can also call the <b>CoCreateInstance</b> function to create a new instance of the <b>TraceDataProviderCollection</b> object. Pass __uuidof(TraceDataProviderCollection) as the class identifier and __uuidof(<b>ITraceDataProviderCollection</b>) as the interface identifier.

To populate the collection with registered providers, call the <a href="https://msdn.microsoft.com/ff35087e-be55-42e8-96e9-c923d06248d8">ITraceDataProviderCollection::GetTraceDataProviders</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceDataProviderCollection</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITraceDataProviderCollection</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/3214f25d-1991-439a-b237-61249a531a2b">Add</a>
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
<a href="https://msdn.microsoft.com/aee595c2-bffc-4c79-89b3-b83f75e58d89">Clear</a>
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
<a href="https://msdn.microsoft.com/553ec66e-d38a-46cc-9b01-f4d7947eda91">Remove</a>
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

<a href="https://msdn.microsoft.com/cd80839a-0cf0-4553-819e-7a8be830b9fa">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d5ecc815-86c1-4a08-b434-88479df3d70c">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of trace providers in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7668d9cc-c1b3-4b72-8e37-305c334905f3">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested trace provider from the collection.

</td>
</tr>
</table> 


## -remarks



To create the object from a script, use the Pla.TraceDataProviderCollection program identifier.



