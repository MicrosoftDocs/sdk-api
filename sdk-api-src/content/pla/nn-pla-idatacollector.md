---
UID: NN:pla.IDataCollector
title: IDataCollector (pla.h)
description: Sets and retrieves collector properties using XML, specifies the log file name, and retrieves the location of the log file.This interface is an abstract class from which the following data collectors derive:IAlertDataCollectorIApiTracingDataCollectorIConfigurationDataCollectorIPerformanceCounterDataCollectorITraceDataCollector
helpviewer_keywords: ["IDataCollector","IDataCollector interface [PLA]","IDataCollector interface [PLA]","described","base.idatacollector","pla.idatacollector","pla/IDataCollector"]
old-location: pla\idatacollector.htm
tech.root: PLA
ms.assetid: e1860bcf-c62d-434b-b98b-38bad7f84d89
ms.date: 12/05/2018
ms.keywords: IDataCollector, IDataCollector interface [PLA], IDataCollector interface [PLA],described, base.idatacollector, pla.idatacollector, pla/IDataCollector
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
 - IDataCollector
 - pla/IDataCollector
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
 - IDataCollector
---

# IDataCollector interface


## -description

Sets and retrieves collector properties using XML, specifies the log file name, and retrieves the location of the log file.

This interface is an abstract class from which the following data collectors derive:<ul>
<li>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iapitracingdatacollector">IApiTracingDataCollector</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iconfigurationdatacollector">IConfigurationDataCollector</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-iperformancecounterdatacollector">IPerformanceCounterDataCollector</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>
</li>
</ul>

## -inheritance

The <b>IDataCollector</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDataCollector</b> also has these types of members:

## -remarks

The following example shows the XML that you can use to initialize this object if you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> property to create one of the derived data collectors. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">IDataCollector::Xml</a> property also returns this XML.


```xml

    <FileName/>
    <FileNameFormat/>
    <FileNameFormatPattern/>
    <Index/>
    <LatestOutputLocation/>
    <LogAppend/>
    <LogCircular/>
    <LogOverwrite/>
    <Name/>
    <OutputLocation/>

```


Note that the example does not show the property elements of the derived data collector (see each data collector for its XML elements). Include these elements in the data collectors XML as appropriate. The following example shows the XML for the alert data collector. You can specify the elements in any order.


```xml
<AlertDataCollector>
    <FileName/>
    <FileNameFormat/>
    <FileNameFormatPattern/>
    <Index/>
    <LatestOutputLocation/>
    <LogAppend/>
    <LogCircular/>
    <LogOverwrite/>
    <Name/>
    <OutputLocation/>
    <Alert/>  <!-- Specify an <Alert> element for each alert -->
    <EventLog/>
    <SampleInterval/>
    <Task/>
    <TaskArguments/>
    <TaskUserTextArguments/>
    <TaskSetWorkingDirectory/>
    <TriggerDataCollectorSet/>
</AlertDataCollector>
```


When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <b>IDataCollector</b>.
