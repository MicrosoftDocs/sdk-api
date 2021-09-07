---
UID: NL:traceloggingactivity.TraceLoggingActivity
title: TraceLoggingActivity
description: Provides support for logging ETW events during an activity. All events must be manually tagged or nested.
helpviewer_keywords: ["TraceLoggingActivity","TraceLoggingActivity class","TraceLoggingActivity class","described","tracelogging.traceloggingactivity","traceloggingactivity/TraceLoggingActivity"]
old-location: tracelogging\traceloggingactivity.htm
tech.root: tracelogging
ms.assetid: 75930876-4DF2-4559-BA06-133FC676B1AD
ms.date: 12/05/2018
ms.keywords: TraceLoggingActivity, TraceLoggingActivity class, TraceLoggingActivity class,described, tracelogging.traceloggingactivity, traceloggingactivity/TraceLoggingActivity
req.header: traceloggingactivity.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2012 R2
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
targetos: Windows
req.typenames: 
req.redist: 
f1_keywords:
 - TraceLoggingActivity
 - traceloggingactivity/TraceLoggingActivity
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - traceloggingactivity.h
api_name:
 - TraceLoggingActivity
---

# TraceLoggingActivity class

## -description

Provides support for logging ETW events during an activity. All events must be manually tagged or nested.

**TraceLoggingActivity** has these types of members:

### Constructors

The **TraceLoggingActivity** class has these constructors.

<table class="members" id="memberListConstructors">
<tr>
<th align="left" width="37%">Constructor</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity(traceloggingactivity__)">TraceLoggingActivity Constructor</a>
</td>
<td align="left" width="63%">
Creates a new <b>TraceLoggingActivity</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity(traceloggingactivity__)">TraceLoggingActivity Constructor</a>
</td>
<td align="left" width="63%">
Transfers ownership of an activity from an existing instance to this instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-traceloggingactivity(traceloggingactivity__)">TraceLoggingActivity Destructor</a>
</td>
<td align="left" width="63%">
Writes a default stop event if the activity has been started, but has not been stopped.

</td>
</tr>
</table> 
<h3><a id="methods"></a>Methods</h3>The <b>TraceLoggingActivity</b> class has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/dn975132(v=vs.85)">TraceLoggingActivity::Id</a>
</td>
<td align="left" width="63%">
Returns a pointer to the activity’s unique identifier (GUID). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/legacy/dn975133(v=vs.85)">TraceLoggingActivity::IsStarted</a>
</td>
<td align="left" width="63%">
Returns true if the activity has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-provider">TraceLoggingActivity::Provider</a>
</td>
<td align="left" width="63%">
Returns the handle to the TraceLogging provider associated with this activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-setrelatedactivity">TraceLoggingActivity::SetRelatedActivity</a>
</td>
<td align="left" width="63%">
Sets the related activity.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingactivity-setrelatedactivityid(constguid)">TraceLoggingActivity::SetRelatedActivityId</a>
</td>
<td align="left" width="63%">
Sets the related activity using the unique identifier.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b>TraceLoggingActivity</b> class has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/tracelogging/keyword-constant">Keyword constant</a>


</td>
<td align="left" width="63%">
The value of the keyword that will be used in the activity’s start and stop events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="/windows/desktop/tracelogging/level-constant">Level constant</a>


</td>
<td align="left" width="63%">
Contains the value of the level that will be used in the activity’s start and stop events.

</td>
</tr>
</table>

## -remarks

In order to use TraceLogging activities, you need to define an instance of either [TraceLoggingThreadActivity](./nl-traceloggingactivity-traceloggingthreadactivity.md). After you have created an instance of one of these classes, you manipulate activity logging using <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingfunction">TraceLoggingFunction</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a>, <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a>, and <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritetagged">TraceLoggingWriteTagged</a>. This class automatically creates a unique identifier when it is started and tracing is turned on.
         

You can nest activities manually by providing unique identifiers to the <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestart">TraceLoggingWriteStart</a> and <a href="/windows/desktop/api/traceloggingactivity/nf-traceloggingactivity-traceloggingwritestop">TraceLoggingWriteStop</a> macros.

## -see-also

[TraceLoggingThreadActivity](./nl-traceloggingactivity-traceloggingthreadactivity.md)
