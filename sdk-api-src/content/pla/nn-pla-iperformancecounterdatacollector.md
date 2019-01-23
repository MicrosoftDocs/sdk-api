---
UID: NN:pla.IPerformanceCounterDataCollector
title: IPerformanceCounterDataCollector
author: windows-sdk-content
description: Specifies the performance counters to query and the log file to which the counter data is written.To create this data collector, call the IDataCollectorCollection::CreateDataCollector or IDataCollectorCollection::CreateDataCollectorFromXml method.
old-location: pla\iperformancecounterdatacollector.htm
tech.root: PLA
ms.assetid: c9a5f417-ffd5-452d-9218-3ac045a55de0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IPerformanceCounterDataCollector, IPerformanceCounterDataCollector interface [PLA], IPerformanceCounterDataCollector interface [PLA],described, base.iperformancecounterdatacollector, pla.iperformancecounterdatacollector, pla/IPerformanceCounterDataCollector
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
 - IPerformanceCounterDataCollector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPerformanceCounterDataCollector interface


## -description


Specifies the performance counters to query and the log file to which the counter data is written.

To create this data collector, call the <a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">IDataCollectorCollection::CreateDataCollector</a> or <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.


## -remarks



The following example shows the XML that you can use to initialize this object if you call <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">CreateDataCollectorFromXml</a> to create it. The <a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">IDataCollector::Xml</a> property also returns this XML.


```xml
<PerformanceCounterDataCollector>
    <DataSourceName/>
    <Counter/>             <!-- Specify this element for each counter -->
    <CounterDisplayName/>  <!-- Read-only. Contains the contents of -->
                           <!-- <PerformanceCounter/> in the user's locale -->
    <LogFileFormat/>
    <SampleInterval/>
    <SegmentMaxRecords/>
</PerformanceCounterDataCollector>
```


Note that the example does not show the property elements inherited from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>. 




## -see-also




<a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a>



<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>
 

 

