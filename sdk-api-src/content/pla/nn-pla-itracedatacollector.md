---
UID: NN:pla.ITraceDataCollector
title: ITraceDataCollector
author: windows-sdk-content
description: Collects trace events from registered providers.This interface defines the trace session.
old-location: pla\itracedatacollector.htm
tech.root: PLA
ms.assetid: 1f57aa92-81f0-445f-baa3-274714e8291e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ITraceDataCollector, ITraceDataCollector interface [PLA], ITraceDataCollector interface [PLA],described, base.itracedatacollector, pla.itracedatacollector, pla/ITraceDataCollector
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
 - ITraceDataCollector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITraceDataCollector interface


## -description


Collects trace events from registered providers.

This interface defines the trace session. The session starts when the data collector set runs. The collection of trace data providers defines the providers that you want to enable to the session when the session runs.

To create this data collector, call the <a href="https://msdn.microsoft.com/b6d98361-3af3-4fb2-ad0b-4449b81d6e9e">IDataCollectorCollection::CreateDataCollector</a> or <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method. For details on the XML that you pass to <b>CreateDataCollectorFromXml</b>, see Remarks.


## -remarks



The following example shows the XML that you can use to initialize this object if you call the <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> method to create it. <a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">The IDataCollector::Xml</a> property also returns this XML.


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


Note that the example does not show the property elements inherited from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a> that you also need to specify.

When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>. 




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>
 

 

