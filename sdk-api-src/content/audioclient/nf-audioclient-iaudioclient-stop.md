---
UID: NF:audioclient.IAudioClient.Stop
title: IAudioClient::Stop (audioclient.h)
description: The Stop method stops the audio stream.
helpviewer_keywords: ["IAudioClient interface [Core Audio]","Stop method","IAudioClient.Stop","IAudioClient::Stop","IAudioClientStop","Stop","Stop method [Core Audio]","Stop method [Core Audio]","IAudioClient interface","audioclient/IAudioClient::Stop","coreaudio.iaudioclient_stop"]
old-location: coreaudio\iaudioclient_stop.htm
tech.root: CoreAudio
ms.assetid: d5824aa9-0b91-4bee-9c0c-26e12a6b96b5
ms.date: 12/05/2018
ms.keywords: IAudioClient interface [Core Audio],Stop method, IAudioClient.Stop, IAudioClient::Stop, IAudioClientStop, Stop, Stop method [Core Audio], Stop method [Core Audio],IAudioClient interface, audioclient/IAudioClient::Stop, coreaudio.iaudioclient_stop
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioClient::Stop
 - audioclient/IAudioClient::Stop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioclient.h
api_name:
 - IAudioClient.Stop
---

# IAudioClient::Stop


## -description

The <b>Stop</b> method stops the audio stream.



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

This method requires prior initialization of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

<b>Stop</b> is a control method that stops a running audio stream. This method stops data from streaming through the client's connection with the audio engine. Stopping the stream freezes the stream's audio clock at its current stream position. A subsequent call to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a> causes the stream to resume running from that position. If necessary, the client can call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-reset">IAudioClient::Reset</a> method to reset the position while the stream is stopped.

For code examples that call the <b>Stop</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/capturing-a-stream">Capturing a Stream</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-reset">IAudioClient::Reset</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a>
