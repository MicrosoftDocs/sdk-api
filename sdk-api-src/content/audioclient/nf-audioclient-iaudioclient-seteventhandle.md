---
UID: NF:audioclient.IAudioClient.SetEventHandle
title: IAudioClient::SetEventHandle (audioclient.h)
description: The SetEventHandle method sets the event handle that the system signals when an audio buffer is ready to be processed by the client.
helpviewer_keywords: ["IAudioClient interface [Core Audio]","SetEventHandle method","IAudioClient.SetEventHandle","IAudioClient::SetEventHandle","IAudioClientSetEventHandle","SetEventHandle","SetEventHandle method [Core Audio]","SetEventHandle method [Core Audio]","IAudioClient interface","audioclient/IAudioClient::SetEventHandle","coreaudio.iaudioclient_seteventhandle"]
old-location: coreaudio\iaudioclient_seteventhandle.htm
tech.root: CoreAudio
ms.assetid: 7bca0c00-5157-43bf-98bd-3bfb23abe860
ms.date: 12/05/2018
ms.keywords: IAudioClient interface [Core Audio],SetEventHandle method, IAudioClient.SetEventHandle, IAudioClient::SetEventHandle, IAudioClientSetEventHandle, SetEventHandle, SetEventHandle method [Core Audio], SetEventHandle method [Core Audio],IAudioClient interface, audioclient/IAudioClient::SetEventHandle, coreaudio.iaudioclient_seteventhandle
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
 - IAudioClient::SetEventHandle
 - audioclient/IAudioClient::SetEventHandle
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
 - IAudioClient.SetEventHandle
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

This method requires prior initialization of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

During stream initialization, the client can, as an option, enable event-driven buffering. To do so, the client calls the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method with the AUDCLNT_STREAMFLAGS_EVENTCALLBACK flag set. After enabling event-driven buffering, and before calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a> method to start the stream, the client must call <b>SetEventHandle</b> to register the event handle that the system will signal each time a buffer becomes ready to be processed by the client.

The event handle should be in the nonsignaled state at the time that the client calls the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">Start</a> method.

If the client has enabled event-driven buffering of a stream, but the client calls the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">Start</a> method for that stream without first calling <b>SetEventHandle</b>, the <b>Start</b> call will fail and return an error code.

If the client does not enable event-driven buffering of a stream but attempts to set an event handle for the stream by calling <b>SetEventHandle</b>, the call will fail and return an error code.

For a code example that calls the <b>SetEventHandle</b> method, see <a href="/windows/desktop/CoreAudio/exclusive-mode-streams">Exclusive-Mode Streams</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-start">IAudioClient::Start</a>