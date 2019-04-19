---
UID: NF:evntprov.EventWrite
title: EventWrite function (evntprov.h)
author: windows-sdk-content
description: Use this function to write an event.
old-location: etw\eventwrite_func.htm
tech.root: ETW
ms.assetid: 93070eb7-c167-4419-abff-e861877dad07
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventWrite, EventWrite function [ETW], base.eventwrite_func, etw.eventwrite_func, evntprov/EventWrite
ms.topic: function
req.header: evntprov.h
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
 - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - API-MS-Win-eventing-provider-l1-1-0.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
 - bcrypt.dll
api_name:
 - EventWrite
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventWrite function


## -description


Use this function to write an event.


## -parameters




### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="https://msdn.microsoft.com/6025c3a6-7d88-49dc-bbc3-655c172dde3c">EventRegister</a>.


### -param EventDescriptor [in]

Metadata that identifies the event to write. For details, see 
      <a href="https://msdn.microsoft.com/907e6c38-5eaa-49da-9dc0-d055dcc69d1a">EVENT_DESCRIPTOR</a>.


### -param UserDataCount [in]

Number of <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a> structures 
      in <i>UserData</i>. The maximum number is 128.


### -param UserData [in, optional]

The event data to write. Allocate a block of memory that contains one or more 
      <a href="https://msdn.microsoft.com/452ce6f6-3857-4f88-b501-44dd6091b97e">EVENT_DATA_DESCRIPTOR</a> structures. Set this 
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



Event data written with this function requires a manifest to consume the data.

ETW decides based on the event descriptor if the event is written to a session (for details, see 
    <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>).

If you call the <a href="https://msdn.microsoft.com/1c412909-bdff-4181-9750-f3444fda4c8f">EventActivityIdControl</a> 
    function to specify an activity identifier for the event, 
    <b>EventWrite</b> retrieves the identifier from thread local 
    storage and includes it with the event.


#### Examples

For an example that uses <b>EventWrite</b>, see 
     <a href="https://msdn.microsoft.com/76e7202e-74ce-40a3-a04b-9af5117fe20e">Writing Manifest-based Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ecdb0e92-fcc1-4b4f-99ea-6812b6b49381">EventWriteString</a>



<a href="https://msdn.microsoft.com/798cf3ba-e1cc-4eaf-a1d2-2313a64aab1a">EventWriteTransfer</a>
 

 

