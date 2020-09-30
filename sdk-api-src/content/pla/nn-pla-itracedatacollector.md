---
UID: NN:pla.ITraceDataCollector
title: ITraceDataCollector (pla.h)
description: Collects trace events from registered providers.This interface defines the trace session.
helpviewer_keywords: ["ITraceDataCollector","ITraceDataCollector interface [PLA]","ITraceDataCollector interface [PLA]","described","base.itracedatacollector","pla.itracedatacollector","pla/ITraceDataCollector"]
old-location: pla\itracedatacollector.htm
tech.root: PLA
ms.assetid: 1f57aa92-81f0-445f-baa3-274714e8291e
ms.date: 12/05/2018
ms.keywords: ITraceDataCollector, ITraceDataCollector interface [PLA], ITraceDataCollector interface [PLA],described, base.itracedatacollector, pla.itracedatacollector, pla/ITraceDataCollector
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
 - ITraceDataCollector
 - pla/ITraceDataCollector
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
 - ITraceDataCollector
---

# ITraceDataCollector interface


## -description

Collects trace events from registered providers.

This interface defines the trace session. The session starts when the data collector set runs. The collection of trace data providers defines the providers that you want to enable to the session when the session runs.

To create this data collector, call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollector">IDataCollectorCollection::CreateDataCollector</a> or <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.

## -remarks

The following example shows the XML that you can use to initialize this object if you call the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> method to create it. <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">The IDataCollector::Xml</a> property also returns this XML.


```xml
<TraceDataCollector>
    <BufferSize/>
    <BuffersLost/>  <!-- Output only -->
    <BuffersWritten/>  <!-- Output only -->
    <ClockType/>
    <EventsLost/>  <!-- Output only -->
    <ExtendedMode/>
    <FlushTimer/>
    <FreeBuffers/>  <!-- Output only -->
    <Guid/>
    <IsKernelTrace/>
    <MaximumBuffers/>
    <MinimumBuffers/>
    <NumberOfBuffers/>
    <PreallocateFile/>
    <ProcessMode/>
    <RealTimeBuffersLost/>  <!-- Output only -->
    <SessionId/>  <!-- Output only -->
    <SessionName/>
    <SessionThreadId/>  <!-- Output only -->
    <StreamMode/>
    <TraceDataProvider>  <!-- Specify for each provider -->
        <DisplayName/>
        <FilterData/>
        <FilterType/>
        <Guid/>
        <KeywordsAll>
            <Description/>
            <ValueMapType/>
            <Value/>
        </KeywordsAll>
        <KeywordsAny>
            <Description/>
            <ValueMapType/>
            <Value/>
        <KeywordsAny/>
        <Level>
            <Description/>
            <ValueMapType/>
            <Value/>
        <Level/>
        <Properties/>
    </TraceDataProvider>
</TraceDataCollector>
```


Note that the example does not show the property elements inherited from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>