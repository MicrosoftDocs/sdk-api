---
UID: NF:evntrace.EnableTraceEx2
title: EnableTraceEx2 function
author: windows-sdk-content
description: Enables or disables the specified event trace provider.
old-location: etw\enabletraceex2.htm
tech.root: ETW
ms.assetid: 3aceffb6-614f-4cad-bbec-f181f0cbdbff
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: EVENT_CONTROL_CODE_CAPTURE_STATE, EVENT_CONTROL_CODE_DISABLE_PROVIDER, EVENT_CONTROL_CODE_ENABLE_PROVIDER, EnableTraceEx2, EnableTraceEx2 function [ETW], TRACE_LEVEL_CRITICAL, TRACE_LEVEL_ERROR, TRACE_LEVEL_INFORMATION, TRACE_LEVEL_VERBOSE, TRACE_LEVEL_WARNING, etw.enabletraceex2, evntrace/EnableTraceEx2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.dll: Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on Windows 8, Windows Server 2012, Windows 7 and Windows Server 2008 R2
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Controller-l1-1-0.dll
 - KernelBase.dll
api_name:
 - EnableTraceEx2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# EnableTraceEx2 function


## -description


The <b>EnableTraceEx2</b> function
    enables or disables the specified event trace provider.

This function supersedes the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> 
    function.


## -parameters




### -param TraceHandle [in]

A handle of the event tracing session to which you want to enable or disable the provider. The 
      <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> function returns this handle. 


### -param ProviderId [in]

A GUID of the event trace provider that you want to enable or disable.


### -param ControlCode [in]

You can specify one of the following control codes:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_CONTROL_CODE_DISABLE_PROVIDER"></a><a id="event_control_code_disable_provider"></a><dl>
<dt><b>EVENT_CONTROL_CODE_DISABLE_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Disables the provider.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_CONTROL_CODE_ENABLE_PROVIDER"></a><a id="event_control_code_enable_provider"></a><dl>
<dt><b>EVENT_CONTROL_CODE_ENABLE_PROVIDER</b></dt>
</dl>
</td>
<td width="60%">
Enables the provider. The session receives events  when the provider is registered.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_CONTROL_CODE_CAPTURE_STATE"></a><a id="event_control_code_capture_state"></a><dl>
<dt><b>EVENT_CONTROL_CODE_CAPTURE_STATE</b></dt>
</dl>
</td>
<td width="60%">
Requests that the provider log its state information. First you would enable the provider and then call 
        <b>EnableTraceEx2</b> with this control code to capture 
        state information.

</td>
</tr>
</table>
 


### -param Level [in]

A provider-defined value that specifies the level of detail included in the event. Specify one of the 
      following levels that are defined in the <i>Winmeta.h</i> header file. Higher numbers imply 
      that you get lower levels as well. For example, if you specify TRACE_LEVEL_WARNING, you also receive all 
      warning, error, and critical events.
     

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

A bitmask of keywords that determine the category of events that you want the provider to write. The 
      provider writes the event if any of the event's keyword bits match any of the bits set in this mask. See 
      Remarks.


### -param MatchAllKeyword [in]

This bitmask is optional. This mask further restricts the category of  events that you want the provider to write. If the event's keyword meets the <i>MatchAnyKeyword</i> condition, the provider will write the event only if all of the bits in this mask exist in the event's keyword. This mask is not used if <i>MatchAnyKeyword</i> is zero. See Remarks.


### -param Timeout [in]

Set to zero to enable the trace asynchronously; this is the default. If the timeout value is zero, this function calls the provider's enable callback and returns immediately. To enable the trace synchronously, specify a timeout value, in milliseconds. If you specify a timeout value, this function calls the provider's enable callback and waits until the callback exits or the timeout expires. To wait forever, set to INFINITE.


### -param EnableParameters [in, optional]

The trace parameters used to enable the provider. For details, see <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> and <a href="https://msdn.microsoft.com/6FC5EF54-2D05-4246-A8E8-7FDA0ABA0D4B">ENABLE_TRACE_PARAMETERS_V1</a>.


## -returns



If the function is successful, the return value is <b>ERROR_SUCCESS</b>.

If the function fails, the return value is one of the 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some 
       common errors and their causes.

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
A parameter is incorrect. 

This can occur if any of the following are true:

<ul>
<li>The <i>ProviderId</i> is <b>NULL</b>.</li>
<li>The <i>TraceHandle</i> is <b>NULL</b>.</li>
</ul>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The timeout value expired before the enable callback completed. For details, see the <i>Timeout</i> parameter.

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
Only users with administrative privileges, users in the <i>Performance Log Users</i> 
         group, and services running as <i>LocalSystem</i>, <i>LocalService</i>, 
         or <i>NetworkService</i> can enable trace providers. To grant a restricted user the ability 
         to enable a trace provider, add them to the <i>Performance Log Users</i> group or see 
         <a href="https://msdn.microsoft.com/699bb165-680f-4d3b-8859-959f319ca4be">EventAccessControl</a>.

<b>Windows XP and Windows 2000:  </b>Anyone can enable a trace provider.

</td>
</tr>
</table>
 




## -remarks



Event trace controllers call this function.

The provider defines its interpretation of being enabled or disabled. Typically, if a provider has been enabled, it generates events, but while it is disabled, it does not. 

Event Tracing for Windows (ETW) supports several categories of filtering.

<ul>
<li>Schematized filtering - This is the traditional filtering setup also called provider-side filtering. The controller defines  a custom set of filters as a binary object that is passed to the provider in the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> call. It is incumbent on the controller and provider to define and interpret these  filters and the controller should only log applicable events. This requires a close coupling of the controller and provider since the type and format of the binary object of what can be filtered is not defined. The <a href="https://msdn.microsoft.com/bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b">TdhEnumerateProviderFilters</a> function can be used to retrieve the filters defined in a manifest.</li>
<li>Scope filtering  - Certain providers are enabled or not enabled to a session based on whether or not they meet the criteria specified by the scope filters. There are several types of scope filters that allow filtering based on the event ID, the process ID (PID), executable filename, the app ID, and the app package name. This feature is supported on Windows 8.1,Windows Server 2012 R2, and later. </li>
<li>Stackwalk filtering - This  notifies ETW to only perform a stack walk for a given set of event IDs. This feature is supported on Windows 8.1,Windows Server 2012 R2, and later. </li>
<li>Event payload filtering  - For manifest providers, events can be filtered on-the-fly based on whether or not they satisfy a logical expression based on one or more predicates.</li>
</ul>
Every time <b>EnableTraceEx2</b> is called, the filters for the provider in that session are replaced by the new parameters defined by the parameters passed to the <b>EnableTraceEx2</b> function. Multiple filters passed in a single <b>EnableTraceEx2</b> call can be combined with an additive effect. To disable filtering and thereby enable all providers/events in the logging session, call <b>EnableTraceEx2</b> with the <i>EnableParameters</i> parameter pointed to an <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> structure with the <b>FilterDescCount</b> member set to 0.

Each filter passed to the <b>EnableTraceEx2</b> function is specified by a <b>Type</b> member in the <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a>. An array of  <b>EVENT_FILTER_DESCRIPTOR</b> structures is passed in the <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> structure passed in the <b>EnableParameters</b> parameter to the <b>EnableTraceEx2</b> function. 

Each type of filter (a specific <b>Type</b> member) may only appear once in a call to the <b>EnableTraceEx2</b> function, however, some filter  types allow multiple conditions to be included in a single filter. The maximum number of filters that can be included in a call to <b>EnableTraceEx2</b> is set by  <b>MAX_EVENT_FILTERS_COUNT</b> defined to be 8 in the <i>Evntprov.h</i> header file. 


Each filter type has its own size or entity limits based on the specific <b>Type</b> member in the <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure.  The list  below indicates these limits.



<table>
<tr>
<th>Term</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_SCHEMATIZED"></a><a id="event_filter_type_schematized"></a><b>EVENT_FILTER_TYPE_SCHEMATIZED</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit: <b>MAX_EVENT_FILTER_DATA_SIZE</b> (1024)</dt>
<dt>Number of elements allowed: Defined by provider and controller</dt>
</dl>
</td>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_PID"></a><a id="event_filter_type_pid"></a><b>EVENT_FILTER_TYPE_PID</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit:  <b>MAX_EVENT_FILTER_DATA_SIZE</b> (1024)</dt>
<dt>Number of elements allowed: <b>MAX_EVENT_FILTER_PID_COUNT</b> (8) </dt>
</dl>
</td>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_EXECUTABLE_NAME"></a><a id="event_filter_type_executable_name"></a><b>EVENT_FILTER_TYPE_EXECUTABLE_NAME</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit:  <b>MAX_EVENT_FILTER_DATA_SIZE</b> (1024)</dt>
<dt>Number of elements allowed: A single string that can contain multiple executable file names separated by semicolons. </dt>
</dl>
</td>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_PACKAGE_ID"></a><a id="event_filter_type_package_id"></a><b>EVENT_FILTER_TYPE_PACKAGE_ID</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit:  <b>MAX_EVENT_FILTER_DATA_SIZE</b> (1024)</dt>
<dt>Number of elements allowed: A single string that can contain multiple package IDs separated by semicolons.</dt>
</dl>
</td>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_PACKAGE_APP_ID"></a><a id="event_filter_type_package_app_id"></a><b>EVENT_FILTER_TYPE_PACKAGE_APP_ID</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit:  <b>MAX_EVENT_FILTER_DATA_SIZE</b> (1024)</dt>
<dt>Number of elements allowed: A single string that can contain multiple package relative app IDs (PRAIDs) separated by semicolons.</dt>
</dl>
</td>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_PAYLOAD"></a><a id="event_filter_type_payload"></a><b>EVENT_FILTER_TYPE_PAYLOAD</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit: 1<b>MAX_EVENT_FILTER_PAYLOAD_SIZE</b> (4096)</dt>
<dt>Number of elements allowed: 1</dt>
</dl>
</td>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_EVENT_ID"></a><a id="event_filter_type_event_id"></a><b>EVENT_FILTER_TYPE_EVENT_ID</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit: Not defined</dt>
<dt>Number of elements allowed: <b>MAX_EVENT_FILTER_EVENT_ID_COUNT</b> (64)</dt>
</dl>
</td>
</tr>
<tr>
<td width="40%">
<a id="EVENT_FILTER_TYPE_STACKWALK"></a><a id="event_filter_type_stackwalk"></a><b>EVENT_FILTER_TYPE_STACKWALK</b>

</td>
<td width="60%">
<dl>
<dt>Filter size limit: Not defined</dt>
<dt>Number of elements allowed: <b>MAX_EVENT_FILTER_EVENT_ID_COUNT</b> (64)</dt>
</dl>
</td>
</tr>
</table>
 

To include all events that a provider provides, set <i>MatchAnyKeyword</i> to zero (for a 
    <a href="about_event_tracing.htm">manifest-based</a> provider or <a href="https://msdn.microsoft.com/8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4">TraceLogging</a> provider 
    and 0xFFFFFFFF for a 
    <a href="about_event_tracing.htm">classic</a> provider). To 
    include specific events, set the <i>MatchAnyKeyword</i> mask to those specific events. To indicate that you wish to enable a Provider Group, use the EVENT_ENABLE_PROPERTY_PROVIDER_GROUP flag on the <b>EnableProperty</b> member of  <i>EnableParameters</i>. For 
    example, if the provider defines an event for its initialization and cleanup routines (set keyword bit 0), an 
    event for its file operations (set keyword bit 1), and an event for its calculation operations (set keyword bit 
    2), you can set <i>MatchAnyKeyword</i> to 5 to receive initialization and cleanup events and 
    calculation events.

If the provider defines more complex event keywords, for example, the provider defines an event that sets bit 
    0 for read and bit 1 for local access and a second event that sets bit 0 for read and bit 2 for remote access, you 
    could set MatchAnyKeyword to 1 to receive all read events, or you could set MatchAnykeyword to 1 and 
    MatchAllKeywords to 3 to receive local reads only.

If an event's keyword is zero, the provider will write the event to the session, regardless of the 
    <i>MatchAnyKeyword</i> and <i>MatchAllKeyword</i> masks.

When you call <b>EnableTraceEx2</b> the provider may or may 
    not be registered. If the provider is registered, ETW calls the provider's callback function, if it implements 
    one, and the session begins receiving events. If the provider is not registered, ETW will call the provider's 
    callback function when it registers itself, if it implements one, and the session will begin receiving events. If 
    the provider is not registered, the provider's callback function will not receive the source ID or filter data. 
    You can call <b>EnableTraceEx2</b> one time to enable a 
    provider before the provider registers itself.

If the provider is registered and already enabled to your session, you can also use this function to update 
    the <i>Level</i>, <i>MatchAnyKeyword</i>, 
    <i>MatchAllKeyword</i> parameters, and the <b>EnableProperty</b> and 
    <b>EnableFilterDesc</b> members of <i>EnableParameters</i>.

On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack 
     walk filters can be used by the <b>EnableTraceEx2</b> 
     function and the <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> and 
     <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structures to filter on 
     specific conditions in a logger session. For more information on event payload filters, see the 
     <a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a>, and 
     <a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a> functions and 
     the <b>ENABLE_TRACE_PARAMETERS</b>, 
     <b>EVENT_FILTER_DESCRIPTOR</b>, and 
     <a href="https://msdn.microsoft.com/6B8C03C9-2936-4FEE-AEF4-ABC368B1CB75">PAYLOAD_FILTER_PREDICATE</a> structures.

You do not call <b>EnableTraceEx2</b> to enable kernel 
     providers. To enable kernel providers, set the <b>EnableFlags</b> member of 
     <a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> which you then pass to 
     <a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>. The 
     <b>StartTrace</b> function enables the selected kernel 
     providers.

Up to eight trace sessions can enable and receive events from the same <a href="about_event_tracing.htm">manifest-based</a> provider or <a href="https://msdn.microsoft.com/8C6A9E91-98F9-4D6B-A937-A22BA7CEB1E4">TraceLogging</a> provider; however, only one trace session can enable a <a href="about_event_tracing.htm">classic</a> provider. If more than one session tried to enable a classic provider, the first session would stop receiving events when the second session enabled the same provider. For example, if Session A enabled Provider 1 and then Session B enabled Provider 1, only Session B would receive events from Provider 1.

The provider remains enabled for the session until the session disables the provider. If the application that started the session ends without disabling the provider, the provider remains enabled.

To determine the level and keywords used to enable a manifest-based provider, use one of the following 
     commands:

<ul>
<li>Logman query providers &lt;provider-name&gt;</li>
<li>Wevtutil gp &lt;provider-name&gt;</li>
</ul>
For classic providers, it is up to the provider to document and make available to potential controllers the severity levels or enable flags that it supports. If the provider wants to be enabled by any controller, the provider should accept 0 for the severity level and enable flags and interpret 0 as a request to perform default logging (whatever that may be).

If you use <b>EnableTraceEx2</b> to enable a classic provider, the following translation occurs:

<ul>
<li>The <i>Level</i> parameter is the same as setting the <i>EnableLevel</i> parameter in <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>.</li>
<li>The <i>MatchAnyKeyword</i> is the same as setting the <i>EnableFlag</i> parameter in <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> except that the keyword value is truncated from a ULONGLONG to a ULONG value.</li>
<li>In the <a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> callback, the provider can call <a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a> to get the level and <a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a> to get the enable flag. </li>
<li>The other parameter are not used.</li>
</ul>
If <b>EnableTraceEx2</b> returns 
     <b>ERROR_INVALID_PARAMETER</b> when enabling filtering, you can turn on tracing to view 
     debugging messages about the failure. This requires a checked build.


#### Examples

The following example shows you how to use the 
     <b>EnableTraceEx2</b> with payload filters using the 
     <a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a> and 
     <a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a> functions to 
     filter on specific conditions in a logger session.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define INITGUID  
#include &lt;windows.h&gt;  
#include &lt;stdlib.h&gt;  
#include &lt;stdio.h&gt;  
#include &lt;strsafe.h&gt;  
#include &lt;evntrace.h&gt;  
#include &lt;tdh.h&gt;  
  
#define MAXIMUM_SESSION_NAME 1024  
  
#define PATH_TO_MANIFEST_FILE L"c:\\ExampleManifest.man"  
  
  
//  
// The following definitions would be found in the include file generated by  
// message compiler from the manifest file.  
//    
//+  
// Provider Example-Provider Event Count 2  
//+  EXTERN_C __declspec(selectany) const GUID EXAMPLE_PROVIDER = {0x37a59b93, 0xbb25, 0x4cee, {0x97, 0xaa, 0x8b, 0x6a, 0xcd, 0xc, 0x4d, 0xf8}};  
  
//  
// Event Descriptors  
//  
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR Example_Event_1 = {0x1, 0x0, 0x0, 0x1, 0x0, 0x0, 0x0};  
#define Example_Event_1_value 0x1  
EXTERN_C __declspec(selectany) const EVENT_DESCRIPTOR Example_Event_2 = {0x2, 0x0, 0x0, 0x1, 0x0, 0x0, 0x0};  
#define Example_Event_2_value 0x2  
  
//  
// (End of snippet from include file)  
//    
  
// Allocate an EVENT_TRACE_PROPERTIES structure and set the needed logging session properties
PEVENT_TRACE_PROPERTIES AllocateTraceProperties (  
    _In_opt_ PWSTR LoggerName,  
    _In_opt_ PWSTR LogFileName  
    )  
{  
    PEVENT_TRACE_PROPERTIES TraceProperties = NULL;  
    ULONG BufferSize;  
  
    BufferSize = sizeof(EVENT_TRACE_PROPERTIES) +   
        (MAXIMUM_SESSION_NAME + MAX_PATH) * sizeof(WCHAR);  
  
    TraceProperties = (PEVENT_TRACE_PROPERTIES)malloc(BufferSize);    
    if (TraceProperties == NULL) {  
        wprintf(L"Unable to allocate %d bytes for properties structure.\n", BufferSize);  
        goto Exit;  
    }  
  
    //      
    // Set the session properties.      
    //    
    ZeroMemory(TraceProperties, BufferSize);  
    TraceProperties-&gt;Wnode.BufferSize = BufferSize;  
    TraceProperties-&gt;Wnode.Flags = WNODE_FLAG_TRACED_GUID;  
    TraceProperties-&gt;LoggerNameOffset = sizeof(EVENT_TRACE_PROPERTIES);  
    TraceProperties-&gt;LogFileNameOffset = sizeof(EVENT_TRACE_PROPERTIES) +   
        (MAXIMUM_SESSION_NAME * sizeof(WCHAR));   
  
    if (LoggerName != NULL) {  
        StringCchCopy((LPWSTR)((PCHAR)TraceProperties + TraceProperties-&gt;LoggerNameOffset),   
                      MAXIMUM_SESSION_NAME,  
                      LoggerName);  
    }  
  
    if (LogFileName != NULL) {  
        StringCchCopy((LPWSTR)((PCHAR)TraceProperties + TraceProperties-&gt;LogFileNameOffset),   
                      MAX_PATH,   
                      LogFileName);  
    }  
  
Exit:  
    return TraceProperties;  
}  

// Free the EVENT_TRACE_PROPERTIES structure previously allocated
VOID FreeTraceProperties (  
    _In_ PEVENT_TRACE_PROPERTIES TraceProperties  
    )  
{  
    free(TraceProperties);  
    return;  
}  

// Set the values needed in a PAYLOAD_FILTER_PREDICATE for a single payload filter  
FORCEINLINE VOID PayloadPredicateCreate(  
    _Out_ PPAYLOAD_FILTER_PREDICATE Predicate,  
    _In_ LPWSTR FieldName,  
    USHORT CompareOp,  
    LPWSTR Value  
)  
{  
    Predicate-&gt;FieldName = FieldName;  
    Predicate-&gt;CompareOp = CompareOp;  
    Predicate-&gt;Value = Value;  
    return;  
}  
  
int __cdecl wmain()  
{  
    UINT i;  
    PVOID EventFilters[2];  
    EVENT_FILTER_DESCRIPTOR FilterDescriptor;  
    UINT PredicateCount;  
    PAYLOAD_FILTER_PREDICATE Predicates[3];  
    ULONG FilterCount;  
    ULONG Status = ERROR_SUCCESS;  
    TRACEHANDLE SessionHandle = 0;  
    PEVENT_TRACE_PROPERTIES TraceProperties;  
    BOOLEAN TraceStarted = FALSE;  
    PWSTR LoggerName = L"MyTrace";  
    ENABLE_TRACE_PARAMETERS EnableParameters;  
  
    ZeroMemory(EventFilters, sizeof(EventFilters));  
    ZeroMemory(Predicates, sizeof(Predicates));  
    TraceProperties = NULL;  
    FilterCount = 0;  
  
    //      
    // Load the manifest for the provider      
    //    
    Status = TdhLoadManifest(PATH_TO_MANIFEST_FILE);  
    if (Status != ERROR_SUCCESS) {  
        wprintf(L"TdhCreatePayloadFilter() failed with %lu\n", Status);  
        goto Exit;  
    }  
  
    //      
    // Create predicates that match the following high-level expression:      
    //      
    // INCLUDE Example_Event_1 IF      
    //     Example_Event_1.Initiator == "User" AND      
    //     7 &lt;= Example_Event_1.Level &lt;= 16      
    //        
    PredicateCount = 0;  
  
    PayloadPredicateCreate(&amp;Predicates[PredicateCount++],  
                           L"Initiator",  
                           PAYLOADFIELD_IS,  
                           L"User");  
  
    PayloadPredicateCreate(&amp;Predicates[PredicateCount++],  
                           L"Level",  
                           PAYLOADFIELD_BETWEEN,  
                           L"7,16");  
  
    Status = TdhCreatePayloadFilter(&amp;EXAMPLE_PROVIDER,  
                                    &amp;Example_Event_1,  
                                    FALSE,      // Match all predicates (AND)                                      PredicateCount,  
                                    Predicates,  
                                    &amp;EventFilters[FilterCount++]);  
    if (Status != ERROR_SUCCESS) {  
        wprintf(L"TdhCreatePayloadFilter() failed with %lu\n", Status);  
        goto Exit;  
    }  
  
    //      
    // Create predicates that match the following high-level expression:      
    // INCLUDE Example_Event_2 IF      
    //      Example_Event_2.Title CONTAINS "UNI" OR      
    //      Example_Event_2.InstanceId == {0E95CFBC-58D4-44BA-BE40-E63A853536DF} OR      
    //      Example_Event_2.ErrorCode != 0      //    
    PredicateCount = 0;  
  
    PayloadPredicateCreate(&amp;Predicates[PredicateCount++],  
                           L"Title",  
                           PAYLOADFIELD_CONTAINS,  
                           L"UNI");  
  
    PayloadPredicateCreate(&amp;Predicates[PredicateCount++],  
                           L"InstanceId",  
                           PAYLOADFIELD_IS,  
                           L" {0E95CFBC-58D4-44BA-BE40-E63A853536DF}");  
  
    PayloadPredicateCreate(&amp;Predicates[PredicateCount++],  
                           L"ErrorCode",  
                           PAYLOADFIELD_NE,  
                           L"0");  
  
    Status = TdhCreatePayloadFilter(&amp;EXAMPLE_PROVIDER,  
                                    &amp;Example_Event_2,  
                                    FALSE,      // Match any predicates (OR)                                      PredicateCount,  
                                    Predicates,  
                                    &amp;EventFilters[FilterCount++]);  
    if (Status != ERROR_SUCCESS) {  
        wprintf(L"TdhCreatePayloadFilter() failed with %lu\n", Status);  
        goto Exit;  
    }  
  
    //      
    // Combine the interim filters into a final filter descriptor.      
    //    
    Status = TdhAggregatePayloadFilters(FilterCount,  
                                        EventFilters,  
                                        NULL,  
                                        &amp;FilterDescriptor);  
    if (Status != ERROR_SUCCESS) {  
        wprintf(L"TdhAggregatePayloadFilters() failed with %lu\n", Status);  
        goto Exit;  
    }  
  
    //      
    // Clean up the interim filters      
    //    
    for (i = 0; i &lt; FilterCount; i++) {  
  
        Status = TdhDeletePayloadFilter(&amp;EventFilters[i]);  
        if (Status != ERROR_SUCCESS) {  
            wprintf(L"TdhDeletePayloadFilter() failed with %lu\n", Status);  
            goto Exit;  
        }  
    }  
  
  
  
    //      
    // Create a new trace session      
    //    
    //      
    // Allocate EVENT_TRACE_PROPERTIES structure and perform some      
    // basic initialization.       
    //      
    // N.B. LoggerName will be populated during StartTrace call.      
    //    
    TraceProperties = AllocateTraceProperties(NULL, L"SystemTrace.etl");  
    if (TraceProperties == NULL) {  
        Status = ERROR_OUTOFMEMORY;  
        goto Exit;  
    }  
  
    TraceProperties-&gt;LogFileMode = EVENT_TRACE_FILE_MODE_SEQUENTIAL | EVENT_TRACE_SYSTEM_LOGGER_MODE;  
    TraceProperties-&gt;MaximumFileSize = 100; // Limit file size to 100MB max      
    TraceProperties-&gt;BufferSize = 512; // Use 512KB trace buffers      
    TraceProperties-&gt;MinimumBuffers = 8;  
    TraceProperties-&gt;MaximumBuffers = 64;  
  
    Status = StartTrace(&amp;SessionHandle, LoggerName, TraceProperties);  
    if (Status != ERROR_SUCCESS) {  
        wprintf(L"StartTrace() failed with %lu\n", Status);  
        goto Exit;  
    }  
  
    TraceStarted = TRUE;  
  
    //      
    // Enable the provider to a trace session with filtering enabled on the      
    // provider      
    //    
    ZeroMemory(&amp;EnableParameters, sizeof(EnableParameters));  
    EnableParameters.Version = ENABLE_TRACE_PARAMETERS_VERSION_2;  
    EnableParameters.EnableFilterDesc = &amp;FilterDescriptor;  
    EnableParameters.FilterDescCount = 1;  
  
    Status = EnableTraceEx2(SessionHandle,  
                            &amp;EXAMPLE_PROVIDER,  
                            EVENT_CONTROL_CODE_ENABLE_PROVIDER,  
                            TRACE_LEVEL_VERBOSE,  
                            0,  
                            0,  
                            0,  
                            &amp;EnableParameters);  
    if (Status != ERROR_SUCCESS) {  
        wprintf(L"EnableTraceEx2() failed with %lu\n", Status);  
        goto Exit;  
    }  
  
    //      
    // Clean up the payload descriptor      
    //    
    Status = TdhCleanupPayloadEventFilterDescriptor(&amp;FilterDescriptor);  
    if (Status != ERROR_SUCCESS) {  
        wprintf(L"TdhCleanupPayloadEventFilterDescriptor() failed with %lu\n", Status);  
        goto Exit;  
    }  
  
    //      
    // Collect trace for 30 seconds      
    //    
    Sleep(30 * 1000);  
  
Exit:  
  
    //      
    // Stop tracing.      
    //    
    if (TraceStarted != FALSE) {  
        Status = ControlTrace(SessionHandle, NULL, TraceProperties, EVENT_TRACE_CONTROL_STOP);    
        if (Status != ERROR_SUCCESS) {  
            wprintf(L"StopTrace() failed with %lu\n", Status);  
        }  
    }  
  
    if (TraceProperties != NULL) {  
        FreeTraceProperties(TraceProperties);  
    }  
  
    TdhUnloadManifest(PATH_TO_MANIFEST_FILE);  
  
    return Status;  
}  
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/6FC5EF54-2D05-4246-A8E8-7FDA0ABA0D4B">ENABLE_TRACE_PARAMETERS_V1</a>



<a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>



<a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>



<a href="https://msdn.microsoft.com/e5c0f2bf-34da-4555-9556-4c79ee9a73ab">GetTraceEnableFlags</a>



<a href="https://msdn.microsoft.com/22326fd9-c428-4430-8a92-978d005f6705">GetTraceEnableLevel</a>



<a href="https://msdn.microsoft.com/6B8C03C9-2936-4FEE-AEF4-ABC368B1CB75">PAYLOAD_FILTER_PREDICATE</a>



<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a>



<a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a>



<a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a>



<a href="https://msdn.microsoft.com/bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b">TdhEnumerateProviderFilters</a>
 

 

