---
UID: NL:traceloggingactivity.TraceLoggingThreadActivity~r1
title: TraceLoggingThreadActivity
author: windows-sdk-content
description: Provides support for logging ETW events during an activity. Events will be automatically tagged with or nested in this activity.
old-location: tracelogging\traceloggingthreadactivity.htm
old-project: tracelogging
ms.assetid: 7666A28B-42B2-473F-852F-BD3F6CAA6AC7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: TraceLoggingThreadActivity, TraceLoggingThreadActivity class, TraceLoggingThreadActivity class,described, tracelogging.traceloggingthreadactivity, traceloggingactivity/TraceLoggingThreadActivity
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: traceloggingactivity.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - traceloggingactivity.h
api_name:
 - TraceLoggingThreadActivity
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
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
<a href="https://msdn.microsoft.com/F57307FB-BC97-475C-8452-41842E4637A1">TraceLoggingThreadActivity Constructor</a>
</td>
<td align="left" width="63%">
Creates a new <b>TraceLoggingThreadActivity</b> object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/A83EE18B-F443-42B8-841D-83CF2BA0FCBC">TraceLoggingThreadActivity Constructor</a>
</td>
<td align="left" width="63%">
Transfers ownership of an activity from an existing instance to a new instance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/BD15FB57-8924-48C5-9735-BF7D378474ED">TraceLoggingThreadActivity Destructor</a>
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
<a href="https://msdn.microsoft.com/A576D2B6-35D1-4195-A20A-533F4D31C5C0">TraceLoggingThreadActivity::Id</a>
</td>
<td align="left" width="63%">
Returns a pointer to the activity’s unique identifier (GUID). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3870A7BC-938F-4319-958F-931418D2E153">TraceLoggingThreadActivity::IsStarted</a>
</td>
<td align="left" width="63%">
Returns true if the activity has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53B0C290-8A1B-4C0A-8EA7-98E26EFF47D1">TraceLoggingThreadActivity::Provider</a>
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

<a href="https://msdn.microsoft.com/DFD096D7-187D-4DC2-A502-C45362FE2A7A">Keyword constant</a>


</td>
<td align="left" width="63%">
The value of the keyword that will be used in the activity’s start and stop events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/DBBBE6C8-B952-493F-AE98-89D54536F1E5">Level constant</a>


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
<a href="https://msdn.microsoft.com/A576D2B6-35D1-4195-A20A-533F4D31C5C0">TraceLoggingThreadActivity::Id</a>
</td>
<td align="left" width="63%">
Returns a pointer to the activity’s unique identifier (GUID). 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3870A7BC-938F-4319-958F-931418D2E153">TraceLoggingThreadActivity::IsStarted</a>
</td>
<td align="left" width="63%">
Returns true if the activity has been started.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/53B0C290-8A1B-4C0A-8EA7-98E26EFF47D1">TraceLoggingThreadActivity::Provider</a>
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

<a href="https://msdn.microsoft.com/DFD096D7-187D-4DC2-A502-C45362FE2A7A">Keyword constant</a>


</td>
<td align="left" width="63%">
The value of the keyword that will be used in the activity’s start and stop events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/DBBBE6C8-B952-493F-AE98-89D54536F1E5">Level constant</a>


</td>
<td align="left" width="63%">
Contains the value of the level that will be used in the activity’s start and stop events.

</td>
</tr>
</table>
<a href="https://msdn.microsoft.com/DFD096D7-187D-4DC2-A502-C45362FE2A7A">Keyword constant</a>


The value of the keyword that will be used in the activity’s start and stop events.


<a href="https://msdn.microsoft.com/DBBBE6C8-B952-493F-AE98-89D54536F1E5">Level constant</a>


Contains the value of the level that will be used in the activity’s start and stop events.

 


## -remarks



This class works by setting a per-thread variable. Only events occurring on the active thread will be automatically tagged.

In order to use TraceLogging activities, you need to define an instance of either <a href="https://msdn.microsoft.com/75930876-4DF2-4559-BA06-133FC676B1AD">TraceLoggingActivity</a> or <b>TraceLoggingThreadActivity</b>. After you have created an instance of one of these classes, you manipulate activity logging using <a href="https://msdn.microsoft.com/70382367-E0A0-4E5B-A14F-863BEC0615C5">TraceLoggingFunction</a>, <a href="https://msdn.microsoft.com/E5B9347E-50A7-49BE-BDD5-DCED39371234">TraceLoggingWriteStart</a>, <a href="https://msdn.microsoft.com/638F08E3-5970-40B3-8025-E3D81ECA1D2A">TraceLoggingWriteStop</a>, and <a href="https://msdn.microsoft.com/BBDFC2B1-33C6-4D5F-AA7B-91BB2A757B1E">TraceLoggingWriteTagged</a>. This class automatically creates a unique identifier when it is started and tracing is turned on.
         

Any active threads will be automatically nested in this instance when you start logging with a <b>TraceLoggingThreadActivity</b> object. In addition, all events will be automatically logged with this object's unique identifier.
         

<div class="alert"><b>Caution</b>  <p class="note">Only use this class when you can guarantee that all activities for this thread are fully nested. You must ensure that no child activity will outlast a parent activity, even in error cases or edge cases.
           

<p class="note">In DEBUG builds, the class will raise an assertion during its Stop event, if it detects incorrect activity nesting, or if the Stop event occurs on a thread other than the thread used to start it.

</div>
<div> </div>
This class is not available for store applications.
         




## -see-also




<a href="https://msdn.microsoft.com/75930876-4DF2-4559-BA06-133FC676B1AD">TraceLoggingActivity Class</a>
 

 

