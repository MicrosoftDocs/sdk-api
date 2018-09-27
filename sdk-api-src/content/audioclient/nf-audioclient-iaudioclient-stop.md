---
UID: NF:audioclient.IAudioClient.Stop
title: IAudioClient::Stop
author: windows-sdk-content
description: The Stop method stops the audio stream.
old-location: coreaudio\iaudioclient_stop.htm
tech.root: CoreAudio
ms.assetid: d5824aa9-0b91-4bee-9c0c-26e12a6b96b5
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IAudioClient interface [Core Audio],Stop method, IAudioClient.Stop, IAudioClient::Stop, IAudioClientStop, Stop, Stop method [Core Audio], Stop method [Core Audio],IAudioClient interface, audioclient/IAudioClient::Stop, coreaudio.iaudioclient_stop
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioclient.h
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient.Stop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioClient::Stop


## -description



The <b>Stop</b> method stops the audio stream.




## -parameters






## -returns



If the method succeeds and stops the stream, it returns S_OK. If the method succeeds and the stream was already stopped, the method returns S_FALSE. If it fails, possible return codes include, but are not limited to, the values shown in the following table.

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
The client has not been successfully initialized.

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

<b>Stop</b> is a control method that stops a running audio stream. This method stops data from streaming through the client's connection with the audio engine. Stopping the stream freezes the stream's audio clock at its current stream position. A subsequent call to <a href="https://msdn.microsoft.com/706f9833-7f06-4bdc-96d5-6872f6effcb9">IAudioClient::Start</a> causes the stream to resume running from that position. If necessary, the client can call the <a href="https://msdn.microsoft.com/c1a4f673-ecbf-4855-b8bb-c0f0807dedd4">IAudioClient::Reset</a> method to reset the position while the stream is stopped.

For code examples that call the <b>Stop</b> method, see the following topics:

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



<a href="https://msdn.microsoft.com/c1a4f673-ecbf-4855-b8bb-c0f0807dedd4">IAudioClient::Reset</a>



<a href="https://msdn.microsoft.com/706f9833-7f06-4bdc-96d5-6872f6effcb9">IAudioClient::Start</a>
 

 

