---
UID: NN:pla.IDataCollectorSet
title: IDataCollectorSet
author: windows-driver-content
description: Manages the configuration information that is common to all data collector objects in the set; adds and removes data collectors from the set; and starts data collection. This is the primary PLA interface that you use.
old-location: pla\idatacollectorset.htm
old-project: PLA
ms.assetid: a4ae0874-4ee6-46a1-9811-8cd4be26859c
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IDataCollectorSet, IDataCollectorSet interface [PLA], IDataCollectorSet interface [PLA],described, base.idatacollectorset, pla.idatacollectorset, pla/IDataCollectorSet
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FolderActionSteps
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Pla.dll
api_name:
-	IDataCollectorSet
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IDataCollectorSet interface


## -description


Manages the configuration information that is common to all data collector objects in the set; adds and 
    removes data collectors from the set; and starts data collection. This is the primary PLA interface that you 
    use.

To get this interface, call the <a href="https://msdn.microsoft.com/7295a55b-12c7-4ed0-a7a4-9ecee16afdec">CoCreateInstance</a> 
    function, passing <code>__uuidof(DataCollectorSet)</code> as the class 
    identifier and <code>__uuidof(IDataCollectorSet)</code> as the interface 
    identifier.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollectorSet</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IDataCollectorSet</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
</td>
<td align="left" width="63%">
Saves, updates, or validates the data collector set. You can also use this method to flush a trace 
     session.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/35e95d41-0d6c-428a-a167-6667275d4fb7">Delete</a>
</td>
<td align="left" width="63%">
Deletes the persisted copy of the data collector set if the set is not running.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597624">GetValue</a>
</td>
<td align="left" width="63%">
Retrieves a user-defined value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406403">Query</a>
</td>
<td align="left" width="63%">
Retrieves the specified data collector set from the hard disk and overwrites this object with the contents 
     of the set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39275154-fe85-492e-9d64-79d17cb4f88d">SetCredentials</a>
</td>
<td align="left" width="63%">
Specifies the user account under which the data collector set runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff597642">SetValue</a>
</td>
<td align="left" width="63%">
Sets a user-defined value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">SetXml</a>
</td>
<td align="left" width="63%">
Sets the property values of those properties included in the XML.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
</td>
<td align="left" width="63%">
Manually starts the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/dn927275">Stop</a>
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

<a href="https://msdn.microsoft.com/1bcfc15e-bc20-4dfa-a934-d0100b8db23f">DataCollectors</a>


</td>
<td align="left" width="63%">
Retrieves the list of data collectors in this set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/739cf386-c5fb-454c-9919-e3997944d68c">DataManager</a>


</td>
<td align="left" width="63%">
Retrieves the data manager associated with this data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


</td>
<td align="left" width="63%">
Retrieves or sets the description of the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/153159b2-54dc-477a-92eb-18328ea3351b">DescriptionUnresolved</a>


</td>
<td align="left" width="63%">
Retrieves the description of the data collector set in its original form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh965535">DisplayName</a>


</td>
<td align="left" width="63%">
Retrieves or sets the display name of the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/47941406-e05d-4a64-9a84-8aa7162e5b48">DisplayNameUnresolved</a>


</td>
<td align="left" width="63%">
Retrieves the display name of the data collector set in its original form.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/afa8f8f2-52a7-481f-ba7e-19f9b757aeb8">Duration</a>


</td>
<td align="left" width="63%">
Retrieves and sets the duration that the data collector set runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0a1203e3-672b-47fb-9072-d3f06ba22865">Keywords</a>


</td>
<td align="left" width="63%">
Retrieves or sets keywords that describe the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c0047144-5f99-4acd-ad96-054afcbe6eb9">LatestOutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves or sets the fully decorated folder name that PLA used the last time logs were written.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh971602">Name</a>


</td>
<td align="left" width="63%">
Retrieves the unique name used to identify the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d0ca2655-f65a-4bcb-8e9e-f247b4207e56">OutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves the decorated folder name if PLA were to create it now.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">RootPath</a>


</td>
<td align="left" width="63%">
Retrieves or sets the base path where the subdirectories are created.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/6654c101-5179-41db-8fd9-ae281691073f">Schedules</a>


</td>
<td align="left" width="63%">
Retrieves the list of schedules that determine when the data collector set runs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/75ebe328-1494-464c-9491-e8a39e1d8ee1">SchedulesEnabled</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates whether the schedules are enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/cd915df3-2823-4d3e-bfd0-545c24f95267">Security</a>


</td>
<td align="left" width="63%">
Retrieves or sets access control information that determines who can access this data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/5ecac3dd-0cd1-4563-a6b3-1b98e29fe769">Segment</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates whether PLA creates new logs if the maximum size or segment 
     duration is reached before the data collector set is stopped.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d958c7a7-0258-4db6-b650-14a61d59221b">SegmentMaxDuration</a>


</td>
<td align="left" width="63%">
Retrieves or sets the duration that the data collector set can run before it begins writing to new log 
     files.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7dd96822-a398-42c3-94f1-b9cd7a647575">SegmentMaxSize</a>


</td>
<td align="left" width="63%">
Retrieves or sets the maximum size of any log file in the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/92bfd307-362e-4d60-9a61-d2096fbb3d19">SerialNumber</a>


</td>
<td align="left" width="63%">
Retrieves or sets the number of times that this data collector set has been started, including 
     segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/43098848-1b1f-4ce1-a34c-62bb493aaf0e">Server</a>


</td>
<td align="left" width="63%">
Retrieves the name of the server where the data collector set is run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/dn265407">Status</a>


</td>
<td align="left" width="63%">
Retrieves the status of the data collector set.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/bb7e18c6-e809-455e-9bee-c4bb6cf07c26">StopOnCompletion</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that determines whether the data collector set stops when all the data collectors 
     in the set are in a completed state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">Subdirectory</a>


</td>
<td align="left" width="63%">
Retrieves or sets a base subdirectory of the root path where the next instance of the data collector set 
     will write its logs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/f9e6eb88-ac38-4b99-ab64-a408f75f7969">SubdirectoryFormat</a>


</td>
<td align="left" width="63%">
Retrieves or sets flags that describe how to decorate the subdirectory name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/83b7df10-8b00-4d64-bf71-2c68e037ab3f">SubdirectoryFormatPattern</a>


</td>
<td align="left" width="63%">
Retrieves or sets a format pattern to use when decorating the folder name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8a89ebb9-2396-43f9-81ee-bfc2cdff18fa">Task</a>


</td>
<td align="left" width="63%">
Retrieves or sets the name of a Task Scheduler job to start each time the data collector set stops, including
    between segments.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">TaskArguments</a>


</td>
<td align="left" width="63%">
Retrieves or sets the command-line arguments to pass to the Task Scheduler job specified in the 
    <a href="https://msdn.microsoft.com/8a89ebb9-2396-43f9-81ee-bfc2cdff18fa">IDataCollectorSet::Task</a> property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/14a7f6db-b5aa-4462-978e-66cd58e05446">TaskRunAsSelf</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that determines whether the task runs as the data collector set user or as the user
    specified in the task.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/99fb2ed4-525b-4733-a652-b164b2c19980">TaskUserTextArguments</a>


</td>
<td align="left" width="63%">
Retrieves or sets the command-line arguments that are substituted for the {usertext} substitution variable in
    the 
    <a href="https://msdn.microsoft.com/7bd045df-379b-40fb-b309-cec531493018">IDataCollectorSet::TaskArguments</a> 
    property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/32fe1dcf-9682-40fd-b301-45385fa33cbe">UserAccount</a>


</td>
<td align="left" width="63%">
Retrieves the user account under which the data collector set will run.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/4b07bf1c-58e8-430a-a68c-c16cab954140">Xml</a>


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
    the <a href="https://msdn.microsoft.com/ac07169e-710c-4267-ae08-ed18a15d866d">IDataCollectorSet::Query</a> method 
    to query the properties of a previously 
    <a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">persisted </a> data collector set.

To create a set, create an instance of the data collector set object and set the properties as appropriate. 
    You
    can set the properties individually or pass XML that contains the property values to the 
    <a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">IDataCollectorSet::SetXml</a> 
    method.

To add new data collector objects to the set, retrieve the collection from the 
    <a href="https://msdn.microsoft.com/1bcfc15e-bc20-4dfa-a934-d0100b8db23f">IDataCollectorSet::DataCollectors</a> 
    property. To persist the data collector set, call the 
    <a href="https://msdn.microsoft.com/7e432e1f-4b86-45dc-93d5-df603068273d">IDataCollectorSet::Commit</a> 
    method.

You can start the data collectors manually using the 
    <a href="https://msdn.microsoft.com/63f0c7b7-0dc6-4491-a2f5-eaae9d22da61">IDataCollectorSet::Start</a> method or automatically 
    using the <a href="https://msdn.microsoft.com/6654c101-5179-41db-8fd9-ae281691073f">IDataCollectorSet::Schedules</a> 
    property. Alternatively, an alert can trigger a collection to run if the 
    <a href="https://msdn.microsoft.com/3ba9b1c0-432e-4caf-a082-33d1c5c3b132">IAlertDataCollector::TriggerDataCollectorSet</a> 
    property is set.

If you want to manage the collected data, retrieve an 
    <a href="https://msdn.microsoft.com/a153d88f-4c7e-45fd-9cd8-497160711de4">IDataManager</a> interface from the 
    <a href="https://msdn.microsoft.com/739cf386-c5fb-454c-9919-e3997944d68c">IDataCollectorSet::DataManager</a> 
    property.

The following example shows the XML elements for a data collector set. For details, see the corresponding 
    property.
   

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;DataCollectorSet&gt;
    &lt;DataManager&gt;
        &lt;Enabled/&gt;              &lt;!-- 0 (false), nonzero (true) --&gt;
        &lt;CheckBeforeRunning/&gt;   &lt;!-- 0 (false), nonzero (true) --&gt;
        &lt;MinFreeDisk/&gt;
        &lt;MaxSize/&gt;
        &lt;MaxFolderCount/&gt;
        &lt;ResourcePolicy/&gt;
        &lt;ReportFileName/&gt;
        &lt;RuleTargetFileName/&gt;
        &lt;EventsFileName/&gt;
        &lt;FolderAction&gt;          &lt;!-- Include a &lt;FolderAction&gt; element for --&gt;
            &lt;Actions/&gt;          &lt;!-- each action to take. --&gt;
            &lt;Age/&gt;
            &lt;SendCabTo/&gt;
            &lt;Size/&gt;
        &lt;/FolderAction&gt;
    &lt;/DataManager&gt;
    &lt;Description/&gt;
    &lt;DescriptionUnresolved/&gt;    &lt;!-- Output only --&gt;
    &lt;DisplayName/&gt;
    &lt;DisplayNameUnresolved/&gt;    &lt;!-- Output only --&gt;
    &lt;Duration/&gt;  
    &lt;Keyword/&gt;                  &lt;!-- Specify for each keyword --&gt;
    &lt;LatestOutputLocation/&gt;     
    &lt;Name/&gt;                     &lt;!-- Output only --&gt;
    &lt;OutputLocation/&gt;           &lt;!-- Output only --&gt;
    &lt;RootPath/&gt;
    &lt;Segment/&gt;
    &lt;SegmentMaxDuration/&gt; 
    &lt;SegmentMaxSize/&gt; 
    &lt;SerialNumber/&gt;
    &lt;Server/&gt;                   &lt;!-- Output only --&gt;
    &lt;Status/&gt;                   &lt;!-- Output only --&gt;
    &lt;Subdirectory/&gt;
    &lt;SubdirectoryFormat/&gt;
    &lt;SubdirectoryFormatPattern/&gt;
    &lt;Task/&gt;
    &lt;TaskArguments/&gt;
    &lt;TaskRunAsSelf/&gt;            &lt;!-- 0 (false), -1 (true) --&gt;
    &lt;TaskUserTextArguments/&gt;
    &lt;Schedule&gt;
        &lt;Days/&gt;
        &lt;EndDate/&gt;              &lt;!-- mm/dd/yyyy --&gt;
        &lt;StartDate/&gt;            &lt;!-- mm/dd/yyyy --&gt;
        &lt;StartTime/&gt;            &lt;!-- hh:mm:ss (use 24-hour clock) --&gt;
    &lt;/Schedule&gt;
    &lt;SchedulesEnabled/&gt;         &lt;!-- 0 (false), nonzero (true) --&gt;
    &lt;Security/&gt;                 &lt;!-- Security Descriptor Definition Language --&gt;
    &lt;StopOnCompletion/&gt;         &lt;!-- 0 (false), nonzero (true) --&gt;
    &lt;UserAccount/&gt;              &lt;!-- Output only. Set using SetCredentials --&gt;&lt;/DataCollectorSet&gt;</pre>
</td>
</tr>
</table></span></div>
If you call <a href="https://msdn.microsoft.com/4b07bf1c-58e8-430a-a68c-c16cab954140">IDataCollectorSet::Xml</a> to 
    retrieve the XML for a set and the set includes data collectors, the XML will also contain the XML elements for 
    each data collector in the set.

To use the data collector set elements to initialize the property values of a data collector set, call the 
    <a href="https://msdn.microsoft.com/10bffd54-990f-412f-baae-b8ab621b02b8">SetXml</a> method. The contents of the XML will 
    overwrite the existing contents of the set. The following shows how to include the elements for the alert data 
    collector. 

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;DataCollectorSet&gt;

    &lt;!-- Data collector set elements go here. --&gt;

    &lt;AlertDataCollector&gt;
        &lt;Alert/&gt;  &lt;!-- Specify an &lt;Alert&gt; element for each alert --&gt;
        &lt;EventLog/&gt;
        &lt;SampleInterval/&gt;
        &lt;Task/&gt;
        &lt;TaskArguments/&gt;
        &lt;TaskRunAsSelf/&gt;            &lt;!-- 0 (false), nonzero (true) --&gt;
        &lt;TaskUserTextArguments/&gt;
        &lt;TriggerDataCollectorSet/&gt;

        &lt;!-- Data collector elements go here. --&gt;
    &lt;/AlertDataCollector&gt;
&lt;/DataCollectorSet&gt;</pre>
</td>
</tr>
</table></span></div>
You can specify only the elements for the properties that you want to set. If you do not specify a property, 
    PLA provides a default value. When you retrieve the XML for the set, the XML includes all elements, including 
    those from the data collectors contained in the set (for details on data collector properties, see each data 
    collector interface). However, the schedule and folder action elements are not included if they are not defined 
    for the set.




## -see-also




<a href="https://msdn.microsoft.com/e1860bcf-c62d-434b-b98b-38bad7f84d89">IDataCollector</a>
 

 

