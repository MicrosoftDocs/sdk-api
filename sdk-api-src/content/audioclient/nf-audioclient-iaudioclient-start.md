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

# IAudioClient::Start


## -description



The <b>Start</b> method starts the audio stream.




## -parameters






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
<dt><b>AUDCLNT_E_NOT_STOPPED</b></dt>
</dl>
</td>
<td width="60%">
The audio stream was not stopped at the time of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_EVENTHANDLE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The audio stream is configured to use event-driven buffering, but the caller has not called <a href="https://msdn.microsoft.com/7bca0c00-5157-43bf-98bd-3bfb23abe860">IAudioClient::SetEventHandle</a> to set the event handle on the stream.

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

<b>Start</b> is a control method that the client calls to start the audio stream. Starting the stream causes the <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> object to begin streaming data between the endpoint buffer and the audio engine. It also causes the stream's audio clock to resume counting from its current position.

The first time this method is called following initialization of the stream, the <a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient</a> object's stream position counter begins at 0. Otherwise, the clock resumes from its position at the time that the stream was last stopped. Resetting the stream forces the stream position back to 0.

To avoid start-up glitches with rendering streams, clients should not call <b>Start</b> until the audio engine has been initially loaded with data by calling the <a href="https://msdn.microsoft.com/c2a0d46b-e8d4-4c51-9810-5580504c9731">IAudioRenderClient::GetBuffer</a> and <a href="https://msdn.microsoft.com/19d89b5e-2e73-4693-b970-7ebf452ef9a1">IAudioRenderClient::ReleaseBuffer</a> methods on the rendering interface.

For code examples that call the <b>Start</b> method, see the following topics:

<ul>
<li>
<a href="https://msdn.microsoft.com/00bfcfd1-6592-43e3-90ad-730c92aa4cd3">Rendering a Stream</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1d9072dc-4f9b-4111-a747-5eb33ad3ae5b">Capturing a Stream</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/5088a3f1-5001-4ed9-a495-9e91df613ab0">IAudioClient Interface</a>



<a href="https://msdn.microsoft.com/eb778503-06f8-4705-9f8d-9a4fd886ae27">IAudioClient::Initialize</a>



<a href="https://msdn.microsoft.com/c2a0d46b-e8d4-4c51-9810-5580504c9731">IAudioRenderClient::GetBuffer</a>



<a href="https://msdn.microsoft.com/19d89b5e-2e73-4693-b970-7ebf452ef9a1">IAudioRenderClient::ReleaseBuffer</a>
 

 

