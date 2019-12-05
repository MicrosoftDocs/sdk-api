---
UID: NN:pla.ITraceDataProvider
title: ITraceDataProvider (pla.h)
description: Specifies a trace provider to enable in the trace session.
old-location: pla\itracedataprovider.htm
tech.root: PLA
ms.assetid: bd2a49c1-8e18-4a14-a797-07f2b9c25812
ms.date: 12/05/2018
ms.keywords: ITraceDataProvider, ITraceDataProvider interface [PLA], ITraceDataProvider interface [PLA],described, base.itracedataprovider, pla.itracedataprovider, pla/ITraceDataProvider
ms.topic: interface
f1_keywords:
- pla/ITraceDataProvider
dev_langs:
- c++
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
- ITraceDataProvider
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ITraceDataProvider interface


## -description


Specifies a trace provider to enable in the trace session.

To get this interface, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovidercollection-createtracedataprovider">ITraceDataProviderCollection::CreateTraceDataProvider</a> method.

You can also use XML to define the provider. For more information, see the Remarks section of <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceDataProvider</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ITraceDataProvider</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ITraceDataProvider</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-getregisteredprocesses">GetRegisteredProcesses</a>
</td>
<td align="left" width="63%">
Retrieves a list of processes that have registered as an Event Tracing for Windows provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-getsecurity">GetSecurity</a>
</td>
<td align="left" width="63%">
Retrieves the security information for the trace data provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-query">Query</a>
</td>
<td align="left" width="63%">
Retrieves details about a registered provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-resolve">Resolve</a>
</td>
<td align="left" width="63%">
Merges the details about a provider with this instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-setsecurity">SetSecurity</a>
</td>
<td align="left" width="63%">
Sets the security information for the trace data provider.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceDataProvider</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_displayname">DisplayName</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the display name of the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_filterdata">FilterData</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets arbitrary data that is sent to the trace data provider for filtering purposes.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_filterenabled">FilterEnabled</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets a value that determines whether the filter data is used to enable the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_filtertype">FilterType</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets a provider-defined filter type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_guid">Guid</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the provider's GUID.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsall">KeywordsAll</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the list of keywords that restricts the category of events that you want the provider to write. The restrictions are in addition to those provided by the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">ITraceDataProvider::KeywordsAny</a> property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_keywordsany">KeywordsAny</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the list of keywords that determine the category of events that you want the provider to write. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_level">Level</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the level of information used to enable the provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedataprovider-get_properties">Properties</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the list of extended data that the provider provides.

</td>
</tr>
</table> 


## -remarks



If you want to retrieve only the display name or GUID of a specific provider or  retrieve only the list of processes registered as that provider, you can get this interface by calling the <b>CoCreateInstance</b> function and passing __uuidof(TraceDataProvider) as the class identifier and __uuidof(ITraceDataProvider) as the interface identifier. To create the object from a script for this purpose, use the Pla.TraceDataProvider program identifier. 

Do not use the <b>CoCreateInstance</b> function if you are going to add the interface to the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a> collection.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-itracedatacollector-get_tracedataproviders">ITraceDataCollector::TraceDataProviders</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-itracedataprovidercollection">ITraceDataProviderCollection</a>
 

 

