---
UID: NN:pla.ITraceDataProviderCollection
title: ITraceDataProviderCollection (pla.h)
author: windows-sdk-content
description: Manages a collection of TraceDataProvider objects.To get this interface, access the ITraceDataCollector::TraceDataProviders property.You can also call the CoCreateInstance function to create a new instance of the TraceDataProviderCollection object.
old-location: pla\itracedataprovidercollection.htm
tech.root: PLA
ms.assetid: 74300222-dca4-4871-bae3-0c3182fbc539
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITraceDataProviderCollection, ITraceDataProviderCollection interface [PLA], ITraceDataProviderCollection interface [PLA],described, base.itracedataprovidercollection, pla.itracedataprovidercollection, pla/ITraceDataProviderCollection
ms.topic: interface
f1_keywords: 
 - "pla/ITraceDataProviderCollection"
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
ms.custom: 19H1
---

# ITraceDataProviderCollection interface


## -description


Manages a collection of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovider">TraceDataProvider</a> objects.

To get this interface, access the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_tracedataproviders">ITraceDataCollector::TraceDataProviders</a> property.

You can also call the <b>CoCreateInstance</b> function to create a new instance of the <b>TraceDataProviderCollection</b> object. Pass __uuidof(TraceDataProviderCollection) as the class identifier and __uuidof(<b>ITraceDataProviderCollection</b>) as the interface identifier.

To populate the collection with registered providers, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-gettracedataproviders">ITraceDataProviderCollection::GetTraceDataProviders</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceDataProviderCollection</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITraceDataProviderCollection</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-add">Add</a>
</td>
<td align="left" width="63%">
Adds a trace provider to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-addrange">AddRange</a>
</td>
<td align="left" width="63%">
Adds one or more trace providers to the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-clear">Clear</a>
</td>
<td align="left" width="63%">
Removes all trace providers from the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-createtracedataprovider">CreateTraceDataProvider</a>
</td>
<td align="left" width="63%">
Creates a trace data provider object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-gettracedataproviders">GetTraceDataProviders</a>
</td>
<td align="left" width="63%">
Populates the collection with registered trace providers.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-gettracedataprovidersbyprocess">GetTraceDataProvidersByProcess</a>
</td>
<td align="left" width="63%">
Populates the collection with the list of providers that have been registered by the specified process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-remove">Remove</a>
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

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-get__newenum">_NewEnum</a>


</td>
<td align="left" width="63%">
Retrieves an interface to the enumeration.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-get_count">Count</a>


</td>
<td align="left" width="63%">
Retrieves the number of trace providers in the collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-get_item">Item</a>


</td>
<td align="left" width="63%">
Retrieves the requested trace provider from the collection.

</td>
</tr>
</table> 


## -remarks



To create the object from a script, use the Pla.TraceDataProviderCollection program identifier.



