---
UID: NF:evntprov.EventWriteString
title: EventWriteString function (evntprov.h)
author: windows-sdk-content
description: Writes an event that contains a string as its data.
old-location: etw\eventwritestring_func.htm
tech.root: ETW
ms.assetid: ecdb0e92-fcc1-4b4f-99ea-6812b6b49381
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: EventWriteString, EventWriteString function [ETW], base.eventwritestring_func, etw.eventwritestring_func, evntprov/EventWriteString
ms.topic: function
f1_keywords: 
 - "evntprov/EventWriteString"
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
api_name:
 - EventWriteString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# EventWriteString function


## -description


Writes an event that contains a string as its data.


## -parameters




### -param RegHandle [in]

Registration handle of the provider. The handle comes from 
      <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventregister">EventRegister</a>.


### -param Level [in]

Level of detail included in the event. If the provider uses a manifest to define the event, set this value 
      to the same level defined in the manifest. If the event is not defined in a manifest, set this value to 0 to 
      ensure the event is written, otherwise, the event is written based on the level rule defined in 
      <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>.


### -param Keyword [in]

Bitmask that specifies the event category. If the provider uses a manifest to define the event, set this 
      value to the same keyword mask defined in the manifest. If the event is not defined in a manifest, set this 
      value to 0 to ensure the event is written, otherwise, the event is written based on the keyword rules defined 
      in <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>.


### -param String [in]

Null-terminated string to write as the event data.


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



The provider does not need a manifest to use this function to write the event, unlike the 
    <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a> function which does require a manifest. 
    Consumers also do not need a manifest to consume events written with this function.

This function gets the acitivity identifier from the thread local storage, if set.

ETW decides based on the level and keyword mask whether  the event is written to a session (for details, see 
    <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>).

This function cannot be used to write events to the Admin or Operational channels.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a>
 

 

