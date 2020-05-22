---
UID: NL:traceloggingactivity.TraceLoggingThreadActivity
title: TraceLoggingThreadActivity (traceloggingactivity.h)
description: Provides support for logging ETW events during an activity. Events will be automatically tagged with or nested in this activity.
helpviewer_keywords: ["TraceLoggingThreadActivity","TraceLoggingThreadActivity class","TraceLoggingThreadActivity class","described","tracelogging.traceloggingthreadactivity","traceloggingactivity/TraceLoggingThreadActivity"]
old-location: tracelogging\traceloggingthreadactivity.htm
tech.root: tracelogging
ms.assetid: 7666A28B-42B2-473F-852F-BD3F6CAA6AC7
ms.date: 12/05/2018
ms.keywords: TraceLoggingThreadActivity, TraceLoggingThreadActivity class, TraceLoggingThreadActivity class,described, tracelogging.traceloggingthreadactivity, traceloggingactivity/TraceLoggingThreadActivity
f1_keywords:
- traceloggingactivity/TraceLoggingThreadActivity
dev_langs:
- c++
req.header: traceloggingactivity.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- traceloggingactivity.h
api_name:
- TraceLoggingThreadActivity
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TraceLoggingThreadActivity class


## -description


Provides support for logging ETW events during an activity. Events will be automatically tagged with or nested in this activity.

<b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingThreadActivity</b> has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Constructors</a></li>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul><h3><a id="constructors"></a>Constructors</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingThreadActivity</b> class has these constructors.
<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975141(v=vs.85)">TraceLoggingThreadActivity Constructor</a>
</td>
<td align="left" width="63%">
Creates a new <b>TraceLoggingThreadActivity</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingthreadactivity-traceloggingthreadactivity(traceloggingthreadactivity__)">TraceLoggingThreadActivity Constructor</a>
</td>
<td align="left" width="63%">
Transfers ownership of an activity from an existing instance to a new instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975140(v=vs.85)">TraceLoggingThreadActivity Destructor</a>
</td>
<td align="left" width="63%">
Writes a default stop event if the activity has been started, but has not been stopped.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>TraceLoggingThreadActivity</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975137(v=vs.85)">TraceLoggingThreadActivity::Id</a>
</td>
<td align="left" width="63%">
Returns a pointer to the activity’s unique identifier (GUID). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975138(v=vs.85)">TraceLoggingThreadActivity::IsStarted</a>
</td>
<td align="left" width="63%">
Returns true if the activity has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingthreadactivity-provider">TraceLoggingThreadActivity::Provider</a>
</td>
<td align="left" width="63%">
Returns the handle to the TraceLogging provider associated with this activity.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingThreadActivity</b> class has these properties.
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
The value of the keyword that will be used in the activity’s start and stop events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/tracelogging/level-constant">Level constant</a>


</td>
<td align="left" width="63%">
Contains the value of the level that will be used in the activity’s start and stop events.

</td>
</tr>
</table> 


## -members

The <b>TraceLoggingThreadActivity</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975137(v=vs.85)">TraceLoggingThreadActivity::Id</a>
</td>
<td align="left" width="63%">
Returns a pointer to the activity’s unique identifier (GUID). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/dn975138(v=vs.85)">TraceLoggingThreadActivity::IsStarted</a>
</td>
<td align="left" width="63%">
Returns true if the activity has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingthreadactivity-provider">TraceLoggingThreadActivity::Provider</a>
</td>
<td align="left" width="63%">
Returns the handle to the TraceLogging provider associated with this activity.

</td>
</tr>
</table>Returns a pointer to the activity’s unique identifier (GUID). 

Returns true if the activity has been started.

Returns the handle to the TraceLogging provider associated with this activity.

 

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">TraceLoggingThreadActivity</b> class has these properties.
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
The value of the keyword that will be used in the activity’s start and stop events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/tracelogging/level-constant">Level constant</a>


</td>
<td align="left" width="63%">
Contains the value of the level that will be used in the activity’s start and stop events.

</td>
</tr>
</table>
<a href="https://docs.microsoft.com/windows/desktop/tracelogging/keyword-constant">Keyword constant</a>


The value of the keyword that will be used in the activity’s start and stop events.


<a href="https://docs.microsoft.com/windows/desktop/tracelogging/level-constant">Level constant</a>


Contains the value of the level that will be used in the activity’s start and stop events.

 


## -remarks



This class works by setting a per-thread variable. Only events occurring on the active thread will be automatically tagged.

In order to use TraceLogging activities, you need to define an instance of either <a href="https://docs.microsoft.com/en-us/windows/win32/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity">TraceLoggingActivity</a> or <b>TraceLoggingThreadActivity</b>. After you have created an instance of one of these classes, you manipulate activity logging using <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingfunction">TraceLoggingFunction</a>, <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a>, <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a>, and <a href="https://docs.microsoft.com/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritetagged">TraceLoggingWriteTagged</a>. This class automatically creates a unique identifier when it is started and tracing is turned on.
         

Any active threads will be automatically nested in this instance when you start logging with a <b>TraceLoggingThreadActivity</b> object. In addition, all events will be automatically logged with this object's unique identifier.
         

<div class="alert"><b>Caution</b>  <p class="note">Only use this class when you can guarantee that all activities for this thread are fully nested. You must ensure that no child activity will outlast a parent activity, even in error cases or edge cases.
           

<p class="note">In DEBUG builds, the class will raise an assertion during its Stop event, if it detects incorrect activity nesting, or if the Stop event occurs on a thread other than the thread used to start it.

</div>
<div> </div>
This class is not available for store applications.
         




## -see-also




<a href="https://docs.microsoft.com/en-us/windows/win32/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity">TraceLoggingActivity Class</a>
 

 

