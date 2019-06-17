---
UID: NF:evntprov.EventWriteEx
title: EventWriteEx function (evntprov.h)
author: windows-sdk-content
description: Use this function to write an event.
old-location: etw\eventwriteex.htm
tech.root: ETW
ms.assetid: 00b907cb-45cd-48c7-bea4-4d8a39b4fa24
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventWriteEx, EventWriteEx function [ETW], etw.eventwriteex, evntprov/EventWriteEx
ms.topic: function
f1_keywords: ["evntprov/EventWriteEx"]
req.header: evntprov.h
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-eventing-provider-l1-1-0.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
 - EventWriteEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventWriteEx function


## -description


Use this function to write an event.


## -parameters




### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>.


### -param EventDescriptor [in]

A descriptor that contains the metadata that identifies the event to write. For details, see 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_descriptor">EVENT_DESCRIPTOR</a>.


### -param Filter [in]

The instance identifiers that identify the session to which the event will not written. Use a bitwise OR 
      to specify multiple identifiers. Set to zero if you do not support filters or if the event is being written to 
      all sessions (no filters failed). For information on getting the identifier for a session, see the 
      <i>FilterData</i> parameter of your 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nc-evntprov-penablecallback">EnableCallback</a> callback.


### -param Flags [in]

Reserved. Must be zero.


### -param ActivityId [in, optional]

GUID that uniquely identifies this activity. If <b>NULL</b>, ETW gets the identifier 
      from the thread local storage. For details on getting this identifier, see 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol">EventActivityIdControl</a>.


### -param RelatedActivityId [in, optional]

Activity identifier from the previous component. Use this parameter to link your component's events to the 
      previous component's events. To get the activity identifier that was set for the previous component, see the 
      descriptions for the <i>ControlCode</i> parameter of the 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol">EventActivityIdControl</a> 
      function.


### -param UserDataCount [in]

Number of <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_data_descriptor">EVENT_DATA_DESCRIPTOR</a> structures 
      in <i>UserData</i>. The maximum number is 128.


### -param UserData [in, optional]

The event data to write. Allocate a block of memory that contains one or more 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_data_descriptor">EVENT_DATA_DESCRIPTOR</a> structures. Set this 
      parameter to <b>NULL</b> if <i>UserDataCount</i> is zero. The data must be 
      in the order specified in the manifest.


## -returns



Returns ERROR_SUCCESS if successful or one of the following values on error.

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
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The registration handle of the provider is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ARITHMETIC_OVERFLOW</b></dt>
</dl>
</td>
<td width="60%">
The event size is larger than the allowed maximum (64k - header).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The session buffer size is too small for the event.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Occurs when filled buffers are trying to flush to disk, but disk IOs are not happening fast enough. This 
        happens when the disk is slow and event traffic is heavy. Eventually, there are no more free (empty) buffers 
        and the event is dropped.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>STATUS_LOG_FILE_FULL</b></dt>
</dl>
</td>
<td width="60%">
The real-time playback file is full. Events are not logged to the session until a real-time consumer 
        consumes the events from the playback file. Do not stop logging events based on this error code.

</td>
</tr>
</table>
 




## -remarks



Event data written with this function requires a manifest. Since the manifest is embedded in the provider, the 
    provider must be available for a consumer  to consume the data written by the provider.

Use the <i>ActivityId</i> and <i>RelatedActivityId</i> parameters when 
    several components want to relate their events in an end-to-end tracing scenario. For example, components A, B, 
    and C perform work on a related activity and want to link their events so that a consumer can consume  all the 
    events related to that activity.  ETW uses thread local storage to make available to the next component the 
    previous component's activity identifier. The component retrieves from the local storage the previous component's 
    identifier and sets the related activity identifier to it. The consumer can then use the related activity 
    identifier to walk the chain of the events from one component to the next.

If each component defined their own activity identifier, the components can make the following calls to link 
     the events:

<ul>
<li>Call the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol">EventActivityIdControl</a> 
      function using the EVENT_ACTIVITY_CTRL_GET_SET_ID control code. The function uses your identifier to set the 
      activity identifier in the thread local storage and returns the activity identifier for the previous component, 
      if set.</li>
<li>Set the <i>RelatedActivityId</i> parameter of this function to the <i>ActivityId</i> value that the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol">EventActivityIdControl</a> function returned. Note that for the first component, the related identifier will be all zeros (GUID_NULL).</li>
<li>Set the <i>ActivityId</i> of this function to <b>NULL</b> to use the activity identifier that you set in thread local storage.</li>
</ul>
A provider can define filters that a session uses to filter events based on event data. With level and keywords, ETW determines whether the event is written to the session but with filters, the provider uses the filter data to determine whether it writes the event to the session. For example, if your provider generates process events, you could define a data filter that filters process events based on the process identifier. If the identifier of the process did not match the identifier that the session passed as filter data, you would set (perform a bitwise OR) the <i>Filter</i> parameter to the session's instance identifier to prevent the event from being written to that session.


#### Examples

For an example that uses <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a>, see 
     <a href="https://docs.microsoft.com/windows/desktop/ETW/writing-manifest-based-events">Writing Manifest-based Events</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwritestring">EventWriteString</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a>
 

 

