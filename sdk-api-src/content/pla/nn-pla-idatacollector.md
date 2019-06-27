---
UID: NN:pla.IDataCollector
title: IDataCollector (pla.h)
author: windows-sdk-content
description: Sets and retrieves collector properties using XML, specifies the log file name, and retrieves the location of the log file.This interface is an abstract class from which the following data collectors derive:IAlertDataCollectorIApiTracingDataCollectorIConfigurationDataCollectorIPerformanceCounterDataCollectorITraceDataCollector
old-location: pla\idatacollector.htm
tech.root: PLA
ms.assetid: e1860bcf-c62d-434b-b98b-38bad7f84d89
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDataCollector, IDataCollector interface [PLA], IDataCollector interface [PLA],described, base.idatacollector, pla.idatacollector, pla/IDataCollector
ms.topic: interface
f1_keywords: 
 - "pla/IDataCollector"
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
 - IDataCollector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDataCollector interface


## -description


Sets and retrieves collector properties using XML, specifies the log file name, and retrieves the location of the log file.

This interface is an abstract class from which the following data collectors derive:<ul>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-ialertdatacollector">IAlertDataCollector</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-iapitracingdatacollector">IApiTracingDataCollector</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-iconfigurationdatacollector">IConfigurationDataCollector</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-iperformancecounterdatacollector">IPerformanceCounterDataCollector</a>
</li>
<li>
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nn-pla-itracedatacollector">ITraceDataCollector</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollector</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IDataCollector</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IDataCollector</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-setxml">SetXml</a>
</td>
<td align="left" width="63%">
Sets the property values of those properties included in the XML. 

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollector</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_datacollectorset">DataCollectorSet</a>


</td>
<td align="left" width="63%">
Retrieves the data collector set to which this data collector belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_datacollectortype">DataCollectorType</a>


</td>
<td align="left" width="63%">
Retrieves the type of this data collector. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filename">FileName</a>


</td>
<td align="left" width="63%">
Retrieves or sets the base name of the file that will contain the data collector data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformat">FileNameFormat</a>


</td>
<td align="left" width="63%">
Retrieves or sets flags that describe how to decorate the file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_filenameformatpattern">FileNameFormatPattern</a>


</td>
<td align="left" width="63%">
Retrieves or sets the format pattern to use when decorating the file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/pla/nf-pla-idatacollector-get_index">Index</a>


</td>
<td align="left" width="63%">
Retrieves the index value of the data collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_latestoutputlocation">LatestOutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves or sets the fully decorated file name that PLA used the last time it created the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logappend">LogAppend</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates if PLA should append the collected data to the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logcircular">LogCircular</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates if PLA should create a circular file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_logoverwrite">LogOverwrite</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates if PLA should overwrite the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_name">Name</a>


</td>
<td align="left" width="63%">
Retrieves or sets the name of the data collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_outputlocation">OutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves the decorated file name if PLA were to create it now.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">Xml</a>


</td>
<td align="left" width="63%">
Retrieves an XML string that describes the values of the data collector properties.

</td>
</tr>
</table> 


## -remarks



The following example shows the XML that you can use to initialize this object if you call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollectorcollection-createdatacollectorfromxml">IDataCollectorCollection::CreateDataCollectorFromXml</a> property to create one of the derived data collectors. The <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/pla/nf-pla-idatacollector-get_xml">IDataCollector::Xml</a> property also returns this XML.


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



