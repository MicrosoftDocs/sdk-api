---
UID: NF:audioclient.IAudioClient.Start
title: IAudioClient::Start (audioclient.h)
description: The Start method starts the audio stream.
helpviewer_keywords: ["IAudioClient interface [Core Audio]","Start method","IAudioClient.Start","IAudioClient::Start","IAudioClientStart","Start","Start method [Core Audio]","Start method [Core Audio]","IAudioClient interface","audioclient/IAudioClient::Start","coreaudio.iaudioclient_start"]
old-location: coreaudio\iaudioclient_start.htm
tech.root: CoreAudio
ms.assetid: 706f9833-7f06-4bdc-96d5-6872f6effcb9
ms.date: 12/05/2018
ms.keywords: IAudioClient interface [Core Audio],Start method, IAudioClient.Start, IAudioClient::Start, IAudioClientStart, Start, Start method [Core Audio], Start method [Core Audio],IAudioClient interface, audioclient/IAudioClient::Start, coreaudio.iaudioclient_start
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
 - IAudioClient::Start
 - audioclient/IAudioClient::Start
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
 - IAudioClient.Start
---

# IAudioClient::Start


## -description

The <b>Start</b> method starts the audio stream.



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
The audio stream was not stopped at the time of the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">Start</a> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_EVENTHANDLE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The audio stream is configured to use event-driven buffering, but the caller has not called <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-seteventhandle">IAudioClient::SetEventHandle</a> to set the event handle on the stream.

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

This method requires prior initialization of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

<b>Start</b> is a control method that the client calls to start the audio stream. Starting the stream causes the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> object to begin streaming data between the endpoint buffer and the audio engine. It also causes the stream's audio clock to resume counting from its current position.

The first time this method is called following initialization of the stream, the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> object's stream position counter begins at 0. Otherwise, the clock resumes from its position at the time that the stream was last stopped. Resetting the stream forces the stream position back to 0.

To avoid start-up glitches with rendering streams, clients should not call <b>Start</b> until the audio engine has been initially loaded with data by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a> and <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-releasebuffer">IAudioRenderClient::ReleaseBuffer</a> methods on the rendering interface.

For code examples that call the <b>Start</b> method, see the following topics:

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



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-releasebuffer">IAudioRenderClient::ReleaseBuffer</a>
