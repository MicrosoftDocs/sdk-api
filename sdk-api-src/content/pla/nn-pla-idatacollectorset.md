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
f1_keywords:
- pla/IDataCollectorSet
dev_langs:
- c++
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
- IDataCollectorSet
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollectorSet interface


## -description


Manages the configuration information that is common to all data collector objects in the set; adds and 
    removes data collectors from the set; and starts data collection. This is the primary PLA interface that you 
    use.

To get this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> 
    function, passing <code>__uuidof(DataCollectorSet)</code> as the class 
    identifier and <code>__uuidof(IDataCollectorSet)</code> as the interface 
    identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollectorSet</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDataCollectorSet</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDataCollectorSet</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">Commit</a>
</td>
<td align="left" width="63%">
Saves, updates, or validates the data collector set. You can also use this method to flush a trace 
     session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-delete">Delete</a>
</td>
<td align="left" width="63%">
Deletes the persisted copy of the data collector set if the set is not running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-getvalue">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves a user-defined value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-query">Query</a>
</td>
<td align="left" width="63%">
Retrieves the specified data collector set from the hard disk and overwrites this object with the contents 
     of the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setcredentials">SetCredentials</a>
</td>
<td align="left" width="63%">
Specifies the user account under which the data collector set runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setvalue">SetValue</a>
</td>
<td align="left" width="63%">
Sets a user-defined value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">SetXml</a>
</td>
<td align="left" width="63%">
Sets the property values of those properties included in the XML.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-start">Start</a>
</td>
<td align="left" width="63%">
Manually starts the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-stop">Stop</a>
</td>
<td align="left" width="63%">
Manually stops the data collector set.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollectorSet</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_datacollectors">DataCollectors</a>


</td>
<td align="left" width="63%">
Retrieves the list of data collectors in this set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_datamanager">DataManager</a>


</td>
<td align="left" width="63%">
Retrieves the data manager associated with this data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_description">Description</a>


</td>
<td align="left" width="63%">
Retrieves or sets the description of the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_descriptionunresolved">DescriptionUnresolved</a>


</td>
<td align="left" width="63%">
Retrieves the description of the data collector set in its original form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_displayname">DisplayName</a>


</td>
<td align="left" width="63%">
Retrieves or sets the display name of the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_displaynameunresolved">DisplayNameUnresolved</a>


</td>
<td align="left" width="63%">
Retrieves the display name of the data collector set in its original form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_duration">Duration</a>


</td>
<td align="left" width="63%">
Retrieves and sets the duration that the data collector set runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_keywords">Keywords</a>


</td>
<td align="left" width="63%">
Retrieves or sets keywords that describe the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_latestoutputlocation">LatestOutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves or sets the fully decorated folder name that PLA used the last time logs were written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_name">Name</a>


</td>
<td align="left" width="63%">
Retrieves the unique name used to identify the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_outputlocation">OutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves the decorated folder name if PLA were to create it now.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_rootpath">RootPath</a>


</td>
<td align="left" width="63%">
Retrieves or sets the base path where the subdirectories are created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedules">Schedules</a>


</td>
<td align="left" width="63%">
Retrieves the list of schedules that determine when the data collector set runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedulesenabled">SchedulesEnabled</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates whether the schedules are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_security">Security</a>


</td>
<td align="left" width="63%">
Retrieves or sets access control information that determines who can access this data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segment">Segment</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates whether PLA creates new logs if the maximum size or segment 
     duration is reached before the data collector set is stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxduration">SegmentMaxDuration</a>


</td>
<td align="left" width="63%">
Retrieves or sets the duration that the data collector set can run before it begins writing to new log 
     files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_segmentmaxsize">SegmentMaxSize</a>


</td>
<td align="left" width="63%">
Retrieves or sets the maximum size of any log file in the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_serialnumber">SerialNumber</a>


</td>
<td align="left" width="63%">
Retrieves or sets the number of times that this data collector set has been started, including 
     segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_server">Server</a>


</td>
<td align="left" width="63%">
Retrieves the name of the server where the data collector set is run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_status">Status</a>


</td>
<td align="left" width="63%">
Retrieves the status of the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_stoponcompletion">StopOnCompletion</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that determines whether the data collector set stops when all the data collectors 
     in the set are in a completed state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectory">Subdirectory</a>


</td>
<td align="left" width="63%">
Retrieves or sets a base subdirectory of the root path where the next instance of the data collector set 
     will write its logs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformat">SubdirectoryFormat</a>


</td>
<td align="left" width="63%">
Retrieves or sets flags that describe how to decorate the subdirectory name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_subdirectoryformatpattern">SubdirectoryFormatPattern</a>


</td>
<td align="left" width="63%">
Retrieves or sets a format pattern to use when decorating the folder name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_task">Task</a>


</td>
<td align="left" width="63%">
Retrieves or sets the name of a Task Scheduler job to start each time the data collector set stops, including
    between segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">TaskArguments</a>


</td>
<td align="left" width="63%">
Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_task">IDataCollectorSet::Task</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskrunasself">TaskRunAsSelf</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that determines whether the task runs as the data collector set user or as the user
    specified in the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskusertextarguments">TaskUserTextArguments</a>


</td>
<td align="left" width="63%">
Retrieves or sets the command-line arguments that are substituted for the {usertext} substitution variable in
    the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_taskarguments">IDataCollectorSet::TaskArguments</a> 
    property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_useraccount">UserAccount</a>


</td>
<td align="left" width="63%">
Retrieves the user account under which the data collector set will run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_xml">Xml</a>


</td>
<td align="left" width="63%">
Retrieves an XML string that describes the values of the data collector set properties, including those of 
     the data collectors contained in the set.

</td>
</tr>
</table> 


## -remarks



To create the object from a script, use the "Pla.DataCollectorSet" program identifier.

To retrieve an existing data collector set, create an instance of the data collector set object and then call 
    the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-query">IDataCollectorSet::Query</a> method 
    to query the properties of a previously 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">persisted </a> data collector set.

To create a set, create an instance of the data collector set object and set the properties as appropriate. 
    You
    can set the properties individually or pass XML that contains the property values to the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">IDataCollectorSet::SetXml</a> 
    method.

To add new data collector objects to the set, retrieve the collection from the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_datacollectors">IDataCollectorSet::DataCollectors</a> 
    property. To persist the data collector set, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-commit">IDataCollectorSet::Commit</a> 
    method.

You can start the data collectors manually using the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-start">IDataCollectorSet::Start</a> method or automatically 
    using the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_schedules">IDataCollectorSet::Schedules</a> 
    property. Alternatively, an alert can trigger a collection to run if the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-ialertdatacollector-get_triggerdatacollectorset">IAlertDataCollector::TriggerDataCollectorSet</a> 
    property is set.

If you want to manage the collected data, retrieve an 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatamanager">IDataManager</a> interface from the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_datamanager">IDataCollectorSet::DataManager</a> 
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


If you call <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-get_xml">IDataCollectorSet::Xml</a> to 
    retrieve the XML for a set and the set includes data collectors, the XML will also contain the XML elements for 
    each data collector in the set.

To use the data collector set elements to initialize the property values of a data collector set, call the 
    <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorset-setxml">SetXml</a> method. The contents of the XML will 
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




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-idatacollector">IDataCollector</a>
 

 

