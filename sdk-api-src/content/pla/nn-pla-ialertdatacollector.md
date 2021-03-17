---
UID: NN:pla.IAlertDataCollector
title: IAlertDataCollector (pla.h)
description: Monitors performance counters and performs actions each time a counter value crosses the specified threshold.To create the alert data collector, call the IDataCollectorCollection::CreateDataCollector or IDataCollectorCollection::CreateDataCollectorFromXml method. For details on the XML that you pass to CreateDataCollectorFromXml, see Remarks.
helpviewer_keywords: ["IAlertDataCollector","IAlertDataCollector interface [PLA]","IAlertDataCollector interface [PLA]","described","base.ialertdatacollector","pla.ialertdatacollector","pla/IAlertDataCollector"]
old-location: pla\ialertdatacollector.htm
tech.root: PLA
ms.assetid: 61907979-fa4a-45da-96c5-7cd12021fbb7
ms.date: 12/05/2018
ms.keywords: IAlertDataCollector, IAlertDataCollector interface [PLA], IAlertDataCollector interface [PLA],described, base.ialertdatacollector, pla.ialertdatacollector, pla/IAlertDataCollector
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
 - IAlertDataCollector
 - pla/IAlertDataCollector
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
 - IAlertDataCollector
---

# IAlertDataCollector interface


## -description

Monitors performance counters and performs actions each time a counter value crosses the specified threshold.

To create the alert data collector, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollector">IDataCollectorCollection::CreateDataCollector</a> or <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.

## -remarks

The following example shows the XML that you can use to initialize this object if you call <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">CreateDataCollectorFromXml</a> to create it. The <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">IDataCollector::Xml</a> property also returns this XML.


```xml
<AlertDataCollector>
    <Alert/>              <!-- Specify an <Alert> element for each alert -->
    <AlertDisplayName/>   <!-- Read-only. Contains the contents of -->
                          <!-- <Alert/> in the user's locale -->
    <EventLog/>           <!-- nonzero (true), 0 (false) -->
    <SampleInterval/>
    <Task/>
    <TaskArguments/>
    <TaskRunAsSelf/>
    <TaskUserTextArguments/>
    <TriggerDataCollectorSet/>
</AlertDataCollector>
```


Note that the example does not show the property elements inherited from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>