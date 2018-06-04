---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IAudioClient::SetEventHandle


## -description



The <b>SetEventHandle</b> method sets the event handle that the system signals when an audio buffer is ready to be processed by the client.




## -parameters




### -param eventHandle [in]

The event handle.


## -returns



If the method succeeds, it returns S_OK. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>eventHandle</i> is <b>NULL</b> or an invalid handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_EVENTHANDLE_NOT_EXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream was not initialized for event-driven buffering.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream has not been successfully initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_DEVICE_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The audio endpoint device has been unplugged, or the audio hardware or associated hardware resources have been reconfigured, disabled, removed, or otherwise made unavailable for use.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_SERVICE_NOT_RUNNING</b></dt>
</dl>
</td>
<td width="60%">
The Windows audio service is not running.

</td>
</tr>
</table>
 




## -remarks



This method requires prior initialization of the <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method.

During stream initialization, the client can, as an option, enable event-driven buffering. To do so, the client calls the <a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a> method with the AUDCLNT_STREAMFLAGS_EVENTCALLBACK flag set. After enabling event-driven buffering, and before calling the <a href="https://msdn.microsoft.com/706f9833-7f06-4bdc-96d5-6872f6effcb9">IAudioClient::Start</a> method to start the stream, the client must call <b>SetEventHandle</b> to register the event handle that the system will signal each time a buffer becomes ready to be processed by the client.

The event handle should be in the nonsignaled state at the time that the client calls the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a> method.

If the client has enabled event-driven buffering of a stream, but the client calls the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a> method for that stream without first calling <b>SetEventHandle</b>, the <b>Start</b> call will fail and return an error code.

If the client does not enable event-driven buffering of a stream but attempts to set an event handle for the stream by calling <b>SetEventHandle</b>, the call will fail and return an error code.

For a code example that calls the <b>SetEventHandle</b> method, see <a href="https://msdn.microsoft.com/196cc6fe-91bf-46fa-acc9-38a7a4005875">Exclusive-Mode Streams</a>.




## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient Interface</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/706f9833-7f06-4bdc-96d5-6872f6effcb9">IAudioClient::Start</a>
 

 

