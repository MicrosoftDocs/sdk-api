---
UID: NF:evntrace.EnableTraceEx
title: EnableTraceEx function (evntrace.h)
description: Enables or disables the specified event trace provider. The EnableTraceEx2 function supersedes this function.helpviewer_keywords: ["EVENT_ENABLE_PROPERTY_SID","EVENT_ENABLE_PROPERTY_TS_ID","EnableTraceEx","EnableTraceEx function [ETW]","TRACE_LEVEL_CRITICAL","TRACE_LEVEL_ERROR","TRACE_LEVEL_INFORMATION","TRACE_LEVEL_VERBOSE","TRACE_LEVEL_WARNING","base.enabletraceex_func","etw.enabletraceex_func","evntrace/EnableTraceEx"]
old-location: etw\enabletraceex_func.htm
tech.root: ETW
ms.assetid: 1c675bf7-f292-49b1-8b60-720499a497fd
ms.date: 12/05/2018
ms.keywords: EVENT_ENABLE_PROPERTY_SID, EVENT_ENABLE_PROPERTY_TS_ID, EnableTraceEx, EnableTraceEx function [ETW], TRACE_LEVEL_CRITICAL, TRACE_LEVEL_ERROR, TRACE_LEVEL_INFORMATION, TRACE_LEVEL_VERBOSE, TRACE_LEVEL_WARNING, base.enabletraceex_func, etw.enabletraceex_func, evntrace/EnableTraceEx
f1_keywords:
- evntrace/EnableTraceEx
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
- EnableTraceEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EnableTraceEx function


## -description


Enables or disables the specified event trace provider.
		
		
	
	

The <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function supersedes this function.


## -parameters




### -param ProviderId [in]

GUID of the event trace provider that you want to enable or disable.


### -param SourceId [in, optional]

GUID that uniquely identifies the session that is enabling or disabling the provider. Can be <b>NULL</b>. If the provider does not implement <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nc-evntprov-penablecallback">EnableCallback</a>, the GUID is not used.


### -param TraceHandle [in]

Handle of the event tracing session to which you want to enable or disable the provider. The 
<a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a> function returns this handle. 


### -param IsEnabled [in]

Set to 1 to receive events  when the provider is registered; otherwise, set to 0 to no longer receive events from the provider.


### -param Level [in]

Provider-defined value that specifies the level of detail included in the event.  


Specify one of the following levels that are defined in Winmeta.h. Higher numbers imply that you get lower levels as well. For example, if you specify TRACE_LEVEL_WARNING, you also receive all warning, error, and critical events.
					

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
 


### -param MatchAnyKeyword [in]

Bitmask of keywords that determine the category of events that you want the provider to write. The provider writes the event if any of the event's keyword bits match any of the bits set in this mask. See Remarks.


### -param MatchAllKeyword [in]

This bitmask is optional. This mask further restricts the category of  events that you want the provider to write. If the event's keyword meets the <i>MatchAnyKeyword</i> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword. This mask is not used if <i>MatchAnyKeyword</i> is zero. See Remarks.


### -param EnableProperty [in]

Optional information that ETW can include when writing the event. The data is written to the <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">extended data item</a> section of the event. To include the optional information, specify one or more of the following flags; otherwise, set to zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_SID"></a><a id="event_enable_property_sid"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_SID</b></dt>
</dl>
</td>
<td width="60%">
Include the security identifier (SID) of the user in the extended data.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_TS_ID"></a><a id="event_enable_property_ts_id"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_TS_ID</b></dt>
</dl>
</td>
<td width="60%">
Include the terminal session identifier in the extended data.

</td>
</tr>
</table>
 


### -param EnableFilterDesc [in, optional]

An <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure that points to the filter data. The provider uses to filter data to prevent events that match the filter criteria from being written to the session; the provider determines the layout of the data and how it applies the filter to the event's data. A session can pass only one filter to the provider.

A session can call the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters">TdhEnumerateProviderFilters</a> function to determine the filters that it can pass to the provider.


## -returns



If the function is successful, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

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
<li><i>ProviderId</i> is <b>NULL</b>.</li>
<li><i>TraceHandle</i> is <b>NULL</b>.</li>
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
You cannot update the level when the provider is not registered.

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
Only users with administrative privileges, users in the Performance Log Users group, and services running as LocalSystem, LocalService, NetworkService can enable trace providers. To grant a restricted user the ability to enable a trace provider, add them to the Performance Log Users group or see <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>.

<b>Windows XP and Windows 2000:  </b>Anyone can enable a trace provider.

</td>
</tr>
</table>
 




## -remarks



Event trace controllers call this function.

The provider defines its interpretation of being enabled or disabled. Typically, if a provider has been enabled, it generates events, but while it is disabled, it does not. 

To include all events that a provider provides, set <i>MatchAnyKeyword</i> to zero (for a <a href="https://docs.microsoft.com/windows/desktop/ETW/about-event-tracing">manifest-based</a> provider and 0xFFFFFFFF for a <a href="https://docs.microsoft.com/windows/desktop/ETW/about-event-tracing">classic</a> provider). To include specific events, set the <i>MatchAnyKeyword</i> mask to those specific events. For example, if the provider defines an event for its initialization and cleanup routines (set keyword bit 0), an event for its file operations (set keyword bit 1), and an event for its calculation operations (set keyword bit 2), you can set <i>MatchAnyKeyword</i> to 5 to receive
initialization and cleanup events and calculation events.

If the provider defines more complex event keywords, for example, the provider defines an event that sets bit 0 for read and bit 1 for local access and a second event that sets bit 0 for read and bit 2 for remote access, you could set MatchAnyKeyword to 1 to receive all read events, or you could set MatchAnykeyword to 1 and MatchAllKeywords to 3 to receive local reads only.

If an event's keyword is zero, the provider will write the event to the session, regardless of the <i>MatchAnyKeyword</i> and <i>MatchAllKeyword</i> masks.

When you call <b>EnableTraceEx</b> the provider may or may  not be registered. If the provider is registered, ETW calls the provider's callback function, if it implements one, and the session begins receiving events. If the provider is not registered, ETW will call the provider's callback function when it registers itself, if it implements one, and the session will begin receiving events. If the provider is not registered, the provider's callback function will not receive the source ID or filter data. You can call <b>EnableTraceEx</b> one time to enable a provider before the provider registers itself.

If the provider is registered and already enabled to your session, you can also use this function to update the <i>Level</i>, <i>MatchAnyKeyword</i>, <i>MatchAllKeyword</i>, <i>EnableProperty</i> and  <i>EnableFilterDesc</i> parameters that determine which events the provider writes.

You do not call <b>EnableTraceEx</b> to enable kernel providers. To enable kernel providers, set the <b>EnableFlags</b> member of <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> which you then pass to <a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a>. The <b>StartTrace</b> function enables the selected kernel providers.

Up to eight trace sessions can enable and receive events from the same <a href="https://docs.microsoft.com/windows/desktop/ETW/about-event-tracing">manifest-based</a> provider; however, only one trace session can enable a <a href="https://docs.microsoft.com/windows/desktop/ETW/about-event-tracing">classic</a> provider. If more than one session tried to enable a classic provider, the first session would stop receiving events when the second session enabled the same provider. For example, if Session A enabled Provider 1 and then Session B enabled Provider 1, only Session B would receive events from Provider 1.

The provider remains enabled for the session until the session disables the provider. If the application that started the session ends without disabling the provider, the provider remains enabled.

To determine the level and keywords used to enable a manifest-based provider, use one of the following commands:

<ul>
<li>Logman query providers &lt;provider-name&gt;</li>
<li>Wevtutil gp &lt;provider-name&gt;</li>
</ul>
For classic providers, it is up to the provider to document and make available to potential controllers the severity levels or enable flags that it supports. If the provider wants to be enabled by any controller, the provider should accept 0 for the severity level and enable flags and interpret 0 as a request to perform default logging (whatever that may be). 

If you use <b>EnableTraceEx</b> to enable a classic provider, the following translation occurs:

<ul>
<li>The <i>Level</i> parameter is the same as setting the <i>EnableLevel</i> parameter in <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a>.</li>
<li>The <i>MatchAnyKeyword</i> is the same as setting the <i>EnableFlag</i> parameter in <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a> except that the keyword value is truncated from a ULONGLONG to a ULONG value.</li>
<li>In the <a href="https://docs.microsoft.com/windows/desktop/ETW/controlcallback">ControlCallback</a> callback, the provider can call <a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceenablelevel">GetTraceEnableLevel</a> to get the level and <a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceenableflags">GetTraceEnableFlags</a> to get the enable flag. </li>
<li>The other parameter are not used.</li>
</ul>
A provider can define filters that a session uses to filter events based on event data. With the level and keywords that you provide, ETW determines whether the event is written to the session but with filters, the provider uses the filter data to determine whether it writes the event to the session. For example, if the provider generates process events, it could define a data filter that filters process events based on the process identifier. If the identifier of the process did not match the identifier that you passed as filter data, the provider would prevent event from being written to your session.

On Windows 8.1,Windows Server 2012 R2, and later, payload filters can be used by the <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function to filter on specific conditions in a logger session. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>
 

 

