---
UID: NN:pla.IDataCollector
title: IDataCollector
author: windows-sdk-content
description: Sets and retrieves collector properties using XML, specifies the log file name, and retrieves the location of the log file.This interface is an abstract class from which the following data collectors derive:IAlertDataCollectorIApiTracingDataCollectorIConfigurationDataCollectorIPerformanceCounterDataCollectorITraceDataCollector
old-location: pla\idatacollector.htm
tech.root: pla
ms.assetid: e1860bcf-c62d-434b-b98b-38bad7f84d89
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDataCollector, IDataCollector interface [PLA], IDataCollector interface [PLA],described, base.idatacollector, pla.idatacollector, pla/IDataCollector
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
 - IDataCollector
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollector interface


## -description


Sets and retrieves collector properties using XML, specifies the log file name, and retrieves the location of the log file.

This interface is an abstract class from which the following data collectors derive:<ul>
<li>
<a href="https://msdn.microsoft.com/61907979-fa4a-45da-96c5-7cd12021fbb7">IAlertDataCollector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/8d600d35-bd2b-44fc-9da4-3c6e50e90b65">IApiTracingDataCollector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7266c02d-0f56-4754-8a67-68394a5f0158">IConfigurationDataCollector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c9a5f417-ffd5-452d-9218-3ac045a55de0">IPerformanceCounterDataCollector</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1f57aa92-81f0-445f-baa3-274714e8291e">ITraceDataCollector</a>
</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDataCollector</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IDataCollector</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/12ed8697-caec-45d5-9ecf-658b3e4ca8ba">SetXml</a>
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

<a href="https://msdn.microsoft.com/d4449953-b982-474b-ac35-b03e39db48c9">DataCollectorSet</a>


</td>
<td align="left" width="63%">
Retrieves the data collector set to which this data collector belongs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/a5ec0e60-555c-4a95-b13d-a22cc8db7c28">DataCollectorType</a>


</td>
<td align="left" width="63%">
Retrieves the type of this data collector. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9208baf8-0bc7-45c4-a912-7b59f4c1ca6a">FileName</a>


</td>
<td align="left" width="63%">
Retrieves or sets the base name of the file that will contain the data collector data.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3a7744a6-feb3-4aea-856d-8496aecc0176">FileNameFormat</a>


</td>
<td align="left" width="63%">
Retrieves or sets flags that describe how to decorate the file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/94e6bb13-fb99-4968-8a7f-fbda1f6ea42e">FileNameFormatPattern</a>


</td>
<td align="left" width="63%">
Retrieves or sets the format pattern to use when decorating the file name.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/05ba4bd2-33e3-4aa0-bca0-a247379b37bd">Index</a>


</td>
<td align="left" width="63%">
Retrieves the index value of the data collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/e451c3a7-aec3-4fa7-9313-730bfac55f19">LatestOutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves or sets the fully decorated file name that PLA used the last time it created the file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c9843647-2c36-4d08-98d0-4df63b054993">LogAppend</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates if PLA should append the collected data to the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d1b35b02-cfda-42a4-bd1d-d837a91861d6">LogCircular</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates if PLA should create a circular file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/17f40639-2e24-4a7e-b934-036d8595bdbf">LogOverwrite</a>


</td>
<td align="left" width="63%">
Retrieves or sets a value that indicates if PLA should overwrite the current file.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/d023fe2f-7b3c-4ce9-9950-ec30ea09181c">Name</a>


</td>
<td align="left" width="63%">
Retrieves or sets the name of the data collector.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c5453d16-4aa4-4c25-bfc7-514693317473">OutputLocation</a>


</td>
<td align="left" width="63%">
Retrieves the decorated file name if PLA were to create it now.  

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">Xml</a>


</td>
<td align="left" width="63%">
Retrieves an XML string that describes the values of the data collector properties.

</td>
</tr>
</table> 


## -remarks



The following example shows the XML that you can use to initialize this object if you call the <a href="https://msdn.microsoft.com/32a1aba6-24f4-416a-b2ba-9be264fce3fc">IDataCollectorCollection::CreateDataCollectorFromXml</a> property to create one of the derived data collectors. The <a href="https://msdn.microsoft.com/c362cd5f-2db3-40ad-8f5e-e75a40db204c">IDataCollector::Xml</a> property also returns this XML.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>
    &lt;FileName/&gt;
    &lt;FileNameFormat/&gt;
    &lt;FileNameFormatPattern/&gt;
    &lt;Index/&gt;
    &lt;LatestOutputLocation/&gt;
    &lt;LogAppend/&gt;
    &lt;LogCircular/&gt;
    &lt;LogOverwrite/&gt;
    &lt;Name/&gt;
    &lt;OutputLocation/&gt;
</pre>
</td>
</tr>
</table></span></div>
Note that the example does not show the property elements of the derived data collector (see each data collector for its XML elements). Include these elements in the data collectors XML as appropriate. The following example shows the XML for the alert data collector. You can specify the elements in any order.

<div class="code"><span codelanguage="XML"><table>
<tr>
<th>XML</th>
</tr>
<tr>
<td>
<pre>&lt;AlertDataCollector&gt;
    &lt;FileName/&gt;
    &lt;FileNameFormat/&gt;
    &lt;FileNameFormatPattern/&gt;
    &lt;Index/&gt;
    &lt;LatestOutputLocation/&gt;
    &lt;LogAppend/&gt;
    &lt;LogCircular/&gt;
    &lt;LogOverwrite/&gt;
    &lt;Name/&gt;
    &lt;OutputLocation/&gt;
    &lt;Alert/&gt;  &lt;!-- Specify an &lt;Alert&gt; element for each alert --&gt;
    &lt;EventLog/&gt;
    &lt;SampleInterval/&gt;
    &lt;Task/&gt;
    &lt;TaskArguments/&gt;
    &lt;TaskUserTextArguments/&gt;
    &lt;TaskSetWorkingDirectory/&gt;
    &lt;TriggerDataCollectorSet/&gt;
&lt;/AlertDataCollector&gt;</pre>
</td>
</tr>
</table></span></div>
When you specify the XML to create the collector, you can specify only the elements for the properties that you want to set. If you do not specify a property, PLA provides a default value. When you retrieve the XML for the collector, the XML provides all elements, including those from <b>IDataCollector</b>. 



