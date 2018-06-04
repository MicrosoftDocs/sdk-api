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

# ITraceDataCollector interface


## -description


Collects trace events from registered providers.

This interface defines the trace session. The session starts when the data collector set runs. The collection of trace data providers defines the providers that you want to enable to the session when the session runs.

To create this data collector, call the <a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">IDataCollectorCollection::CreateDataCollector</a> or <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.


## -remarks



The following example shows the XML that you can use to initialize this object if you call the <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method to create it. <a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">The IDataCollector::Xml</a> property also returns this XML.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;TraceDataCollector&gt;
    &lt;BufferSize/&gt;
    &lt;BuffersLost/&gt;  &lt;!-- Output only --&gt;
    &lt;BuffersWritten/&gt;  &lt;!-- Output only --&gt;
    &lt;ClockType/&gt;
    &lt;EventsLost/&gt;  &lt;!-- Output only --&gt;
    &lt;ExtendedMode/&gt;
    &lt;FlushTimer/&gt;
    &lt;FreeBuffers/&gt;  &lt;!-- Output only --&gt;
    &lt;Guid/&gt;
    &lt;IsKernelTrace/&gt;
    &lt;MaximumBuffers/&gt;
    &lt;MinimumBuffers/&gt;
    &lt;NumberOfBuffers/&gt;
    &lt;PreallocateFile/&gt;
    &lt;ProcessMode/&gt;
    &lt;RealTimeBuffersLost/&gt;  &lt;!-- Output only --&gt;
    &lt;SessionId/&gt;  &lt;!-- Output only --&gt;
    &lt;SessionName/&gt;
    &lt;SessionThreadId/&gt;  &lt;!-- Output only --&gt;
    &lt;StreamMode/&gt;
    &lt;TraceDataProvider&gt;  &lt;!-- Specify for each provider --&gt;
        &lt;DisplayName/&gt;
        &lt;FilterData/&gt;
        &lt;FilterType/&gt;
        &lt;Guid/&gt;
        &lt;KeywordsAll&gt;
            &lt;Description/&gt;
            &lt;ValueMapType/&gt;
            &lt;Value/&gt;
        &lt;/KeywordsAll&gt;
        &lt;KeywordsAny&gt;
            &lt;Description/&gt;
            &lt;ValueMapType/&gt;
            &lt;Value/&gt;
        &lt;KeywordsAny/&gt;
        &lt;Level&gt;
            &lt;Description/&gt;
            &lt;ValueMapType/&gt;
            &lt;Value/&gt;
        &lt;Level/&gt;
        &lt;Properties/&gt;
    &lt;/TraceDataProvider&gt;
&lt;/TraceDataCollector&gt;</pre>
</td>
</tr>
</table></span></div>
Note that the example does not show the property elements inherited from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>. 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>
 

 

