---
UID: NN:pla.ITraceDataProvider
title: ITraceDataProvider
author: windows-sdk-content
description: Specifies a trace provider to enable in the trace session.
old-location: pla\itracedataprovider.htm
tech.root: PLA
ms.assetid: bd2a49c1-8e18-4a14-a797-07f2b9c25812
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: ITraceDataProvider, ITraceDataProvider interface [PLA], ITraceDataProvider interface [PLA],described, base.itracedataprovider, pla.itracedataprovider, pla/ITraceDataProvider
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceDataProvider interface


## -description


Specifies a trace provider to enable in the trace session.

To get this interface, call the <a href="https://msdn.microsoft.com/234de4d8-896f-462d-8785-8b768697bf2e">ITraceDataProviderCollection::CreateTraceDataProvider</a> method.

You can also use XML to define the provider. For more information, see the Remarks section of <a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITraceDataProvider</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ITraceDataProvider</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/f848f209-c761-41aa-8e9f-4b7e2ecb54ae">GetRegisteredProcesses</a>
</td>
<td align="left" width="63%">
Retrieves a list of processes that have registered as an Event Tracing for Windows provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2f1618db-aa43-4cac-a652-db172781e988">GetSecurity</a>
</td>
<td align="left" width="63%">
Retrieves the security information for the trace data provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b3d1720f-3a74-4040-803b-266bd0d50cfc">Query</a>
</td>
<td align="left" width="63%">
Retrieves details about a registered provider.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cabe7207-30f9-4382-bc29-b435d6e4c218">Resolve</a>
</td>
<td align="left" width="63%">
Merges the details about a provider with this instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/07b6f5b3-5531-4174-9315-661695bd7c5d">SetSecurity</a>
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

<a href="https://msdn.microsoft.com/1a162b71-d4e3-4259-9980-bf40766983b1">DisplayName</a>


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

<a href="https://msdn.microsoft.com/a5b1c141-d820-4435-be1e-93f2ae69d1e1">FilterData</a>


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

<a href="https://msdn.microsoft.com/fef5e6a4-3a97-4799-b46d-c0e82b1c0104">FilterEnabled</a>


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

<a href="https://msdn.microsoft.com/adc9f89f-fffe-4df0-a9fd-72ae80fdf9b5">FilterType</a>


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

<a href="https://msdn.microsoft.com/0d2166dc-24cf-4d5f-8b37-94c4f9990178">Guid</a>


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

<a href="https://msdn.microsoft.com/9ff48234-927b-4b87-a9b8-2a1047b5e3de">KeywordsAll</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the list of keywords that restricts the category of events that you want the provider to write. The restrictions are in addition to those provided by the <a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">ITraceDataProvider::KeywordsAny</a> property. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/10159c09-609a-4263-a515-241ab942c3e8">KeywordsAny</a>


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

<a href="https://msdn.microsoft.com/5e9390c4-12d4-4087-b4c8-5f58c2522a93">Level</a>


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

<a href="https://msdn.microsoft.com/1dc21423-fa55-4312-b86a-63d4f59e4cf1">Properties</a>


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

Do not use the <b>CoCreateInstance</b> function if you are going to add the interface to the <a href="https://msdn.microsoft.com/74300222-dca4-4871-bae3-0c3182fbc539">ITraceDataProviderCollection</a> collection.




## -see-also




<a href="https://msdn.microsoft.com/7a2006e8-3c4c-4441-8c9e-be9ce584dd63">ITraceDataCollector::TraceDataProviders</a>



<a href="https://msdn.microsoft.com/74300222-dca4-4871-bae3-0c3182fbc539">ITraceDataProviderCollection</a>
 

 

