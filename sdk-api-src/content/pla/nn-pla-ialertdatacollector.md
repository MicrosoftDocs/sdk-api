---
UID: NN:pla.IAlertDataCollector
title: IAlertDataCollector
author: windows-sdk-content
description: Monitors performance counters and performs actions each time a counter value crosses the specified threshold.To create the alert data collector, call the IDataCollectorCollection::CreateDataCollector or IDataCollectorCollection::CreateDataCollectorFromXml method. For details on the XML that you pass to CreateDataCollectorFromXml, see Remarks.
old-location: pla\ialertdatacollector.htm
old-project: PLA
ms.assetid: 61907979-fa4a-45da-96c5-7cd12021fbb7
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IAlertDataCollector, IAlertDataCollector interface [PLA], IAlertDataCollector interface [PLA],described, base.ialertdatacollector, pla.ialertdatacollector, pla/IAlertDataCollector
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: pla.h
req.include-header: 
req.redist: 
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
 - IAlertDataCollector
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: ADAM
---

# IAlertDataCollector interface


## -description


Monitors performance counters and performs actions each time a counter value crosses the specified threshold.

To create the alert data collector, call the <a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">IDataCollectorCollection::CreateDataCollector</a> or <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.


## -remarks



The following example shows the XML that you can use to initialize this object if you call <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">CreateDataCollectorFromXml</a> to create it. The <a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">IDataCollector::Xml</a> property also returns this XML.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;AlertDataCollector&gt;
    &lt;Alert/&gt;              &lt;!-- Specify an &lt;Alert&gt; element for each alert --&gt;
    &lt;AlertDisplayName/&gt;   &lt;!-- Read-only. Contains the contents of --&gt;
                          &lt;!-- &lt;Alert/&gt; in the user's locale --&gt;
    &lt;EventLog/&gt;           &lt;!-- nonzero (true), 0 (false) --&gt;
    &lt;SampleInterval/&gt;
    &lt;Task/&gt;
    &lt;TaskArguments/&gt;
    &lt;TaskRunAsSelf/&gt;
    &lt;TaskUserTextArguments/&gt;
    &lt;TriggerDataCollectorSet/&gt;
&lt;/AlertDataCollector&gt;</pre>
</td>
</tr>
</table></span></div>
Note that the example does not show the property elements inherited from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>. 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>
 

 

