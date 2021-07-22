---
UID: NN:pla.IDataCollectorSet
title: IDataCollectorSet (pla.h)
description: Manages the configuration information that is common to all data collector objects in the set; adds and removes data collectors from the set; and starts data collection. This is the primary PLA interface that you use.
helpviewer_keywords: ["IDataCollectorSet","IDataCollectorSet interface [PLA]","IDataCollectorSet interface [PLA]","described","base.idatacollectorset","pla.idatacollectorset","pla/IDataCollectorSet"]
old-location: pla\idatacollectorset.htm
tech.root: PLA
ms.assetid: a4ae0874-4ee6-46a1-9811-8cd4be26859c
ms.date: 12/05/2018
ms.keywords: IDataCollectorSet, IDataCollectorSet interface [PLA], IDataCollectorSet interface [PLA],described, base.idatacollectorset, pla.idatacollectorset, pla/IDataCollectorSet
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
 - IDataCollectorSet
 - pla/IDataCollectorSet
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
 - IDataCollectorSet
---

# IDataCollectorSet interface


## -description

Manages the configuration information that is common to all data collector objects in the set; adds and 
    removes data collectors from the set; and starts data collection. This is the primary PLA interface that you 
    use.

To get this interface, call the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> 
    function, passing <code>__uuidof(DataCollectorSet)</code> as the class 
    identifier and <code>__uuidof(IDataCollectorSet)</code> as the interface 
    identifier.

## -inheritance

The <b>IDataCollectorSet</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDataCollectorSet</b> also has these types of members:

## -remarks

To create the object from a script, use the "Pla.DataCollectorSet" program identifier.

To retrieve an existing data collector set, create an instance of the data collector set object and then call 
    the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-query">IDataCollectorSet::Query</a> method 
    to query the properties of a previously 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">persisted </a> data collector set.

To create a set, create an instance of the data collector set object and set the properties as appropriate. 
    You
    can set the properties individually or pass XML that contains the property values to the 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">IDataCollectorSet::SetXml</a> 
    method.

To add new data collector objects to the set, retrieve the collection from the 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_datacollectors">IDataCollectorSet::DataCollectors</a> 
    property. To persist the data collector set, call the 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a> 
    method.

You can start the data collectors manually using the 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-start">IDataCollectorSet::Start</a> method or automatically 
    using the <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedules">IDataCollectorSet::Schedules</a> 
    property. Alternatively, an alert can trigger a collection to run if the 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_triggerdatacollectorset">IAlertDataCollector::TriggerDataCollectorSet</a> 
    property is set.

If you want to manage the collected data, retrieve an 
    <a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a> interface from the 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_datamanager">IDataCollectorSet::DataManager</a> 
    property.

The following example shows the XML elements for a data collector set. For details, see the corresponding 
    property.
   


```xml
<DataCollectorSet>
    <DataManager>
        <Enabled/>              <!-- 0 (false), nonzero (true) -->
        <CheckBeforeRunning/>   <!-- 0 (false), nonzero (true) -->
        <MinFreeDisk/>
        <MaxSize/>
        <MaxFolderCount/>
        <ResourcePolicy/>
        <ReportFileName/>
        <RuleTargetFileName/>
        <EventsFileName/>
        <FolderAction>          <!-- Include a <FolderAction> element for -->
            <Actions/>          <!-- each action to take. -->
            <Age/>
            <SendCabTo/>
            <Size/>
        </FolderAction>
    </DataManager>
    <Description/>
    <DescriptionUnresolved/>    <!-- Output only -->
    <DisplayName/>
    <DisplayNameUnresolved/>    <!-- Output only -->
    <Duration/>  
    <Keyword/>                  <!-- Specify for each keyword -->
    <LatestOutputLocation/>     
    <Name/>                     <!-- Output only -->
    <OutputLocation/>           <!-- Output only -->
    <RootPath/>
    <Segment/>
    <SegmentMaxDuration/> 
    <SegmentMaxSize/> 
    <SerialNumber/>
    <Server/>                   <!-- Output only -->
    <Status/>                   <!-- Output only -->
    <Subdirectory/>
    <SubdirectoryFormat/>
    <SubdirectoryFormatPattern/>
    <Task/>
    <TaskArguments/>
    <TaskRunAsSelf/>            <!-- 0 (false), -1 (true) -->
    <TaskUserTextArguments/>
    <Schedule>
        <Days/>
        <EndDate/>              <!-- mm/dd/yyyy -->
        <StartDate/>            <!-- mm/dd/yyyy -->
        <StartTime/>            <!-- hh:mm:ss (use 24-hour clock) -->
    </Schedule>
    <SchedulesEnabled/>         <!-- 0 (false), nonzero (true) -->
    <Security/>                 <!-- Security Descriptor Definition Language -->
    <StopOnCompletion/>         <!-- 0 (false), nonzero (true) -->
    <UserAccount/>              <!-- Output only. Set using SetCredentials --></DataCollectorSet>
```


If you call <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_xml">IDataCollectorSet::Xml</a> to 
    retrieve the XML for a set and the set includes data collectors, the XML will also contain the XML elements for 
    each data collector in the set.

To use the data collector set elements to initialize the property values of a data collector set, call the 
    <a href="/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">SetXml</a> method. The contents of the XML will 
    overwrite the existing contents of the set. The following shows how to include the elements for the alert data 
    collector. 


```xml
<DataCollectorSet>

    <!-- Data collector set elements go here. -->

    <AlertDataCollector>
        <Alert/>  <!-- Specify an <Alert> element for each alert -->
        <EventLog/>
        <SampleInterval/>
        <Task/>
        <TaskArguments/>
        <TaskRunAsSelf/>            <!-- 0 (false), nonzero (true) -->
        <TaskUserTextArguments/>
        <TriggerDataCollectorSet/>

        <!-- Data collector elements go here. -->
    </AlertDataCollector>
</DataCollectorSet>
```


You can specify only the elements for the properties that you want to set. If you do not specify a property, 
    PLA provides a default value. When you retrieve the XML for the set, the XML includes all elements, including 
    those from the data collectors contained in the set (for details on data collector properties, see each data 
    collector interface). However, the schedule and folder action elements are not included if they are not defined 
    for the set.

## -see-also

<a href="/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>
