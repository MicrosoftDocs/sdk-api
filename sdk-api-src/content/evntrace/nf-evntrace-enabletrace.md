---
UID: NF:evntrace.EnableTrace
title: EnableTrace function
author: windows-sdk-content
description: Enables or disables the specified classic event trace provider. On Windows Vista and later, call the EnableTraceEx function to enable or disable a provider.
old-location: etw\enabletrace.htm
tech.root: ETW
ms.assetid: d75f18e1-e5fa-4039-bb74-76dea334b0fd
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: EnableTrace, EnableTrace function [ETW], TRACE_LEVEL_CRITICAL, TRACE_LEVEL_ERROR, TRACE_LEVEL_INFORMATION, TRACE_LEVEL_VERBOSE, TRACE_LEVEL_WARNING, _evt_enabletrace, base.enabletrace, etw.enabletrace, evntrace/EnableTrace
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-eventing-Legacy-l1-1-0.dll
 - advapi32legacy.dll
api_name:
 - EnableTrace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnableTrace function


## -description


Enables or disables the specified classic event trace provider. 
		

On Windows Vista and later, call the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> function to enable or disable a provider.


## -parameters




### -param Enable [in]

If <b>TRUE</b>, the provider is enabled; otherwise, the provider is disabled.


### -param EnableFlag [in]

Provider-defined value that specifies the class of events for which the provider generates events. A provider that generates only one class of events will typically ignore this flag. If the provider is more complex, the provider could use the <i>TraceGuidReg</i> parameter of <a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> to register more than one class of events. For example, if the provider has a database component, a UI component, and a general processing component, the provider could register separate event classes for these components. This would then allow the controller the ability to turn on tracing in only the database component. 

The provider calls <a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a> from its <a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> function to obtain the enable flags.


### -param EnableLevel [in]

Provider-defined value that specifies the level of information the event generates. For example, you can use this value to indicate the severity level of the events (informational, warning, error) you want the provider to generate. 




Specify a value from zero to 255. ETW defines the following severity levels that you can use. Higher numbers imply that you get lower levels as well. For example, if you specify TRACE_LEVEL_WARNING, you also receive all warning, error, and fatal events.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_CRITICAL"></a><a id="trace_level_critical"></a><dl>
<dt><b>TRACE_LEVEL_CRITICAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Abnormal exit or termination events

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_ERROR"></a><a id="trace_level_error"></a><dl>
<dt><b>TRACE_LEVEL_ERROR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Severe error events

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_WARNING"></a><a id="trace_level_warning"></a><dl>
<dt><b>TRACE_LEVEL_WARNING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Warning events such as allocation failures

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_INFORMATION"></a><a id="trace_level_information"></a><dl>
<dt><b>TRACE_LEVEL_INFORMATION</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Non-error events such as entry or exit events

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_VERBOSE"></a><a id="trace_level_verbose"></a><dl>
<dt><b>TRACE_LEVEL_VERBOSE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Detailed trace events

</td>
</tr>
</table>
 


### -param ControlGuid [in]

GUID of the event trace provider that you want to enable or disable.


### -param TraceHandle

TBD




#### - SessionHandle [in]

Handle of the event tracing session to which you want to enable, disable, or change the logging level of the provider. The 
<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> function returns this handle.


## -returns



If the function is successful, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true: 




<ul>
<li><i>ControlGuid</i> is <b>NULL</b>.</li>
<li><i>SessionHandle</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FUNCTION</b></dt>
</dl>
</td>
<td width="60%">
You cannot change the enable flags and level when the provider is not registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_GUID_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The provider is not registered.  Occurs when <a href="Http://go.microsoft.com/fwlink/p/?linkid=83987">KB307331</a> or Windows 2000 Service Pack 4 is installed and the 
provider is not registered. To avoid this error, the provider must first be registered. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES </b></dt>
</dl>
</td>
<td width="60%">
Exceeded the number of trace sessions that can enable the provider.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Only users with administrative privileges, users in the Performance Log Users group, and services running as LocalSystem, LocalService, NetworkService can enable trace providers. To grant a restricted user the ability to enable a trace provider, add them to the Performance Log Users group or see <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>.

<b>Windows XP and Windows 2000:  </b>Anyone can enable a trace provider.

</td>
</tr>
</table>
 




## -remarks



Event trace controllers call this function.

Up to eight trace sessions can enable and receive events from the same <a href="about_event_tracing.htm">manifest-based</a> provider; however, only one trace session can enable a <a href="about_event_tracing.htm">classic</a> provider. If more than one session tried to enable a classic provider, the first session would stop receiving events when the second session enabled the same provider. For example, if Session A enabled Provider 1 and then Session B enabled Provider 1, only Session B would receive events from Provider 1.

The provider remains enabled for the session until the session disables the provider. If the application that started the session ends without disabling the provider, the provider remains enabled.

The 
<b>EnableTrace</b> function calls the 
<a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> function implemented by the event trace provider, if defined. The provider defines its interpretation of being enabled or disabled. Typically, if a provider has been enabled, it generates events, but while it is disabled, it does not. The 
<b>ControlCallback</b> function can call the 
<a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a>, 
<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a>, and 
<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a> functions to obtain the values specified for the <i>EnableFlag</i>, <i>EnableLevel</i>, and <i>SessionHandle</i> parameters, respectively.

You can call this function one time to enable a provider before the provider registers itself. After the provider registers itself, ETW calls the provider's <a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> function. If you try to enable the provider for multiple sessions before the provider registers itself, ETW will only enable the provider for the last session. For example, if you enable the provider to Session A and then enable the provider to Session B, when the provider registers itself, the provider is only enabled for Session B.

You do not call <b>EnableTrace</b> to enable kernel providers. To enable kernel providers, set the <b>EnableFlags</b> member of <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> which you then pass to <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>. The <b>StartTrace</b> function enables the selected kernel providers.

To determine the level and keywords used to enable a manifest-based provider, use one of the following commands:

<ul>
<li>Logman query providers &lt;provider-name&gt;</li>
<li>Wevtutil gp &lt;provider-name&gt;</li>
</ul>
For classic providers, it is up to the provider to document and make available to potential controllers the severity levels or enable flags that it supports. If the provider wants to be enabled by any controller, the provider should accept 0 for the severity level and enable flags and interpret 0 as a request to perform default logging (whatever that may be). 

If you use <b>EnableTrace</b> to enable a manifest-based provider, the following translation occurs:<ul>
<li>The <i>EnableLevel</i> parameter is the same as setting the <i>Level</i> parameter in <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>.</li>
<li>The <i>EnableFlag</i> is the same as setting the <i>MatchAnyKeyword</i> parameter in <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>.</li>
<li>In the <a href="https://msdn.microsoft.com/f339323e-9da9-495f-aac5-f44969a018eb">EnableCallback</a> callback, the <i>SourceId</i> parameter will be <b>NULL</b>, <i>Level</i> will be set to the value in <b>EnableTrace</b>, <i>MatchAnyKeyword</i> will be set to the value of <i>EnableFlag</i> in <a href="https://msdn.microsoft.com/03eea902-5050-4ab2-8a72-9bff7777e234">EventTrace</a>, <i>MatchAllKeyword</i> will be 0, and <i>FilterData</i> will be <b>NULL</b>. </li>
</ul>


On Windows 8.1,Windows Server 2012 R2, and later, payload filters can be used by the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function to filter on specific conditions in a logger session. 


#### Examples

For an example that uses 
<b>EnableTrace</b>, see 
<a href="https://msdn.microsoft.com/13c83b62-9235-4101-82a9-a118e6ece3d5">Example that Creates a Session and Enables a manifest-based provider</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a>



<a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>



<a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a>



<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a>



<a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a>



<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>
 

 

