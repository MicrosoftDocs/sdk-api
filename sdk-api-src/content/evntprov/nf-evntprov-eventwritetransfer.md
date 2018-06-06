---
UID: NF:evntprov.EventWriteTransfer
title: EventWriteTransfer function
author: windows-sdk-content
description: Links events together when tracing events in an end-to-end scenario.
old-location: etw\eventwritetransfer_func.htm
old-project: ETW
ms.assetid: 798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EventWriteTransfer, EventWriteTransfer function [ETW], base.eventwritetransfer_func, etw.eventwritetransfer_func, evntprov/EventWriteTransfer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: EVENT_INFO_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-provider-l1-1-0.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
 - EventWriteTransfer
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# EventWriteTransfer function


## -description



		Links events together when tracing events in an end-to-end scenario.


## -parameters




### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="https://msdn.microsoft.com/6025c3a6-7d88-49dc-bbc3-655c172dde3c">EventRegister</a>.


### -param EventDescriptor [in]

Metadata that identifies the event to write. For details, see 
      <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param ActivityId [in, optional]

GUID that uniquely identifies this activity. If <b>NULL</b>, ETW gets the identifier 
      from the thread local storage. For details on getting this identifier, see 
      <a href="https://msdn.microsoft.com/1c412909-bdff-4181-9750-f3444fda4c8f">EventActivityIdControl</a>.


### -param RelatedActivityId [in, optional]

Activity identifier from the previous component. Use this parameter to link your component's events to the 
      previous component's events. To get the activity identifier that was set for the previous component, see the 
      descriptions for the <i>ControlCode</i> parameter of the 
      <a href="https://msdn.microsoft.com/1c412909-bdff-4181-9750-f3444fda4c8f">EventActivityIdControl</a> 
      function.


### -param UserDataCount [in]

Number of <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a> structures 
      in <i>UserData</i>. The maximum number is 128.


### -param UserData [in, optional]

The event data to write. Allocate a block of memory that contains one or more 
      <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a> structures. Set this 
      parameter to <b>NULL</b> if <i>UserDataCount</i> is zero. The data must 
      be in the order specified in the manifest.


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



Beginning with Windows 7 and Windows Server 2008 R2, use 
    <a href="https://msdn.microsoft.com/00b907cb-45cd-48c7-bea4-4d8a39b4fa24">EventWriteEx</a> to write transfer events in an end-to-end 
    scenario.

Use this function when several components want to relate their events in an end-to-end tracing scenario. For 
    example, components A, B, and C perform work on a related activity and want to link their events so that a 
    consumer can consume  all the events related to that activity.  ETW uses thread local storage to make available 
    to the next component the previous component's activity identifier. The component retrieves from the local 
    storage the previous component's identifier and sets the related activity identifier to it. The consumer can then 
    use the related activity identifier to walk the chain of the events from one component to the next.

If each component defined their own activity identifier, the components can make the following calls to link 
     the events:

<ul>
<li>Call the <a href="https://msdn.microsoft.com/1c412909-bdff-4181-9750-f3444fda4c8f">EventActivityIdControl</a> 
      function using the EVENT_ACTIVITY_CTRL_GET_SET_ID control code. The function uses your identifier to set the activity identifier in the thread local storage and returns the activity identifier for the previous component, if set. </li>
<li>Set the <i>RelatedActivityId</i> parameter of this function to the <i>ActivityId</i> value that the <a href="https://msdn.microsoft.com/1c412909-bdff-4181-9750-f3444fda4c8f">EventActivityIdControl</a> function returned. Note that for the first component, the related identifier will be all zeros (GUID_NULL).</li>
<li>Set the <i>ActivityId</i> of this function to <b>NULL</b> to use the activity identifier that you set in thread local storage.</li>
</ul>
Event data written with this function requires a manifest. Since the manifest is embedded in the provider, the provider must be available for a consumer  to consume the data written by the provider.

ETW decides based on the event descriptor if the event is written to a session (for details, see 
    <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>).




## -see-also




<a href="https://msdn.microsoft.com/1c412909-bdff-4181-9750-f3444fda4c8f">EventActivityIdControl</a>



<a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a>



<a href="https://msdn.microsoft.com/ecdb0e92-fcc1-4b4f-99ea-6812b6b49381">EventWriteString</a>
 

 

