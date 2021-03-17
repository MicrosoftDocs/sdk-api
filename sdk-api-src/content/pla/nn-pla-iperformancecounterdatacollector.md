---
UID: NN:pla.IPerformanceCounterDataCollector
title: IPerformanceCounterDataCollector (pla.h)
description: Specifies the performance counters to query and the log file to which the counter data is written.To create this data collector, call the IDataCollectorCollection::CreateDataCollector or IDataCollectorCollection::CreateDataCollectorFromXml method.
helpviewer_keywords: ["IPerformanceCounterDataCollector","IPerformanceCounterDataCollector interface [PLA]","IPerformanceCounterDataCollector interface [PLA]","described","base.iperformancecounterdatacollector","pla.iperformancecounterdatacollector","pla/IPerformanceCounterDataCollector"]
old-location: pla\iperformancecounterdatacollector.htm
tech.root: PLA
ms.assetid: c9a5f417-ffd5-452d-9218-3ac045a55de0
ms.date: 12/05/2018
ms.keywords: IPerformanceCounterDataCollector, IPerformanceCounterDataCollector interface [PLA], IPerformanceCounterDataCollector interface [PLA],described, base.iperformancecounterdatacollector, pla.iperformancecounterdatacollector, pla/IPerformanceCounterDataCollector
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IPerformanceCounterDataCollector
 - pla/IPerformanceCounterDataCollector
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IPerformanceCounterDataCollector
---

# IPerformanceCounterDataCollector interface


## -description

Specifies the performance counters to query and the log file to which the counter data is written.

To create this data collector, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollector">IDataCollectorCollection::CreateDataCollector</a> or <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.

## -remarks

The following example shows the XML that you can use to initialize this object if you call <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">CreateDataCollectorFromXml</a> to create it. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">IDataCollector::Xml</a> property also returns this XML.


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


Note that the example does not show the property elements inherited from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>



<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>