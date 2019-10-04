---
UID: NL:traceloggingactivity.TraceLoggingActivity~r1
title: TraceLoggingActivity
author: windows-sdk-content
description: TBD
tech.root:
ms.assetid: b5fb71bf-1906-4b9d-a845-b8bd92e8042d
ms.author: windowssdkdev
ms.date: 
ms.topic: class
f1_keywords: 
 - "traceloggingactivity/TraceLoggingActivity"
dev_langs:
 - c++
req.header: traceloggingactivity.h
req.include-header:
req.redist:
req.target-type:
req.target-min-winverclnt:
req.target-min-winversvr:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library: 
topic_type: 
 - apiref
api_type: 
 - COM
api_location: 
 - traceloggingactivity.h
api_name: 
 - TraceLoggingActivity
targetos: Windows
---

# TraceLoggingActivity class

## -description

Provides support for logging ETW events during an activity. All events must be manually tagged or nested.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingActivity</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingActivity</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity(traceloggingactivity__)">TraceLoggingActivity Constructor</a>
</td>
<td align="left" width="63%">
Creates a new <b>TraceLoggingActivity</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity(traceloggingactivity__)">TraceLoggingActivity Constructor</a>
</td>
<td align="left" width="63%">
Transfers ownership of an activity from an existing instance to this instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity(traceloggingactivity__)">TraceLoggingActivity Destructor</a>
</td>
<td align="left" width="63%">
Writes a default stop event if the activity has been started, but has not been stopped.

</td>
</tr>
</table>�
<h3><a id="methods"></a>Methods</h3>The <b>TraceLoggingActivity</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975132(v=vs.85)">TraceLoggingActivity::Id</a>
</td>
<td align="left" width="63%">
Returns a pointer to the activity�s unique identifier (GUID). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975133(v=vs.85)">TraceLoggingActivity::IsStarted</a>
</td>
<td align="left" width="63%">
Returns true if the activity has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-provider">TraceLoggingActivity::Provider</a>
</td>
<td align="left" width="63%">
Returns the handle to the TraceLogging provider associated with this activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-setrelatedactivity">TraceLoggingActivity::SetRelatedActivity</a>
</td>
<td align="left" width="63%">
Sets the related activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-setrelatedactivityid(constguid)">TraceLoggingActivity::SetRelatedActivityId</a>
</td>
<td align="left" width="63%">
Sets the related activity using the unique identifier.

</td>
</tr>
</table>�
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingActivity</b> class has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/tracelogging/keyword-constant">Keyword constant</a>


</td>
<td align="left" width="63%">
The value of the keyword that will be used in the activity�s start and stop events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/tracelogging/level-constant">Level constant</a>


</td>
<td align="left" width="63%">
Contains the value of the level that will be used in the activity�s start and stop events.

</td>
</tr>
</table>�


## -inheritance
TraceLoggingActivity interits from _TlgActivityBase. 
## -members

The <b>TraceLoggingActivity</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975132(v=vs.85)">TraceLoggingActivity::Id</a>
</td>
<td align="left" width="63%">
Returns a pointer to the activity�s unique identifier (GUID). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975133(v=vs.85)">TraceLoggingActivity::IsStarted</a>
</td>
<td align="left" width="63%">
Returns true if the activity has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-provider">TraceLoggingActivity::Provider</a>
</td>
<td align="left" width="63%">
Returns the handle to the TraceLogging provider associated with this activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-setrelatedactivity">TraceLoggingActivity::SetRelatedActivity</a>
</td>
<td align="left" width="63%">
Sets the related activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-setrelatedactivityid(constguid)">TraceLoggingActivity::SetRelatedActivityId</a>
</td>
<td align="left" width="63%">
Sets the related activity using the unique identifier.

</td>
</tr>
</table>Returns a pointer to the activity�s unique identifier (GUID). 

Returns true if the activity has been started.

Returns the handle to the TraceLogging provider associated with this activity.

Sets the related activity.

Sets the related activity using the unique identifier.

�

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingActivity</b> class has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/tracelogging/keyword-constant">Keyword constant</a>


</td>
<td align="left" width="63%">
The value of the keyword that will be used in the activity�s start and stop events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/tracelogging/level-constant">Level constant</a>


</td>
<td align="left" width="63%">
Contains the value of the level that will be used in the activity�s start and stop events.

</td>
</tr>
</table>
<a href="https://docs.microsoft.com/windows/desktop/tracelogging/keyword-constant">Keyword constant</a>


The value of the keyword that will be used in the activity�s start and stop events.


<a href="https://docs.microsoft.com/windows/desktop/tracelogging/level-constant">Level constant</a>


Contains the value of the level that will be used in the activity�s start and stop events.



## -remarks

In order to use TraceLogging activities, you need to define an instance of either <b>TraceLoggingActivity</b> or <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity~r1">TraceLoggingThreadActivity</a>. After you have created an instance of one of these classes, you manipulate activity logging using <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingfunction">TraceLoggingFunction</a>, <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a>, <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritetagged">TraceLoggingWriteTagged</a>. This class automatically creates a unique identifier when it is started and tracing is turned on.
         

You can nest activities manually by providing unique identifiers to the <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a> and <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a> macros.
         



## -see-also


<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nl-traceloggingactivity-traceloggingthreadactivity~r1">TraceLoggingThreadActivity Class</a>
�
