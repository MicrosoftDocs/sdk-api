---
UID: NF:audioclient.IAudioRenderClient.GetBuffer
title: IAudioRenderClient::GetBuffer (audioclient.h)
description: Retrieves a pointer to the next available space in the rendering endpoint buffer into which the caller can write a data packet.
helpviewer_keywords: ["GetBuffer","GetBuffer method [Core Audio]","GetBuffer method [Core Audio]","IAudioRenderClient interface","IAudioRenderClient interface [Core Audio]","GetBuffer method","IAudioRenderClient.GetBuffer","IAudioRenderClient::GetBuffer","IAudioRenderClientGetBuffer","audioclient/IAudioRenderClient::GetBuffer","coreaudio.iaudiorenderclient_getbuffer"]
old-location: coreaudio\iaudiorenderclient_getbuffer.htm
tech.root: CoreAudio
ms.assetid: c2a0d46b-e8d4-4c51-9810-5580504c9731
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [Core Audio], GetBuffer method [Core Audio],IAudioRenderClient interface, IAudioRenderClient interface [Core Audio],GetBuffer method, IAudioRenderClient.GetBuffer, IAudioRenderClient::GetBuffer, IAudioRenderClientGetBuffer, audioclient/IAudioRenderClient::GetBuffer, coreaudio.iaudiorenderclient_getbuffer
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
 - IAudioRenderClient::GetBuffer
 - audioclient/IAudioRenderClient::GetBuffer
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
 - IAudioRenderClient.GetBuffer
---

# IAudioRenderClient::GetBuffer


## -description

Retrieves a pointer to the next available space in the rendering endpoint buffer into which the caller can write a data packet.

## -parameters

### -param NumFramesRequested [in]

The number of audio frames in the data packet that the caller plans to write to the requested space in the buffer. If the call succeeds, the size of the buffer area pointed to by <i>*ppData</i> matches the size specified in <i>NumFramesRequested</i>.

### -param ppData [out]

Pointer to a pointer variable into which the method writes the starting address of the buffer area into which the caller will write the data packet.

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
<dt><b>AUDCLNT_E_BUFFER_ERROR</b></dt>
</dl>
</td>
<td width="60%">

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">GetBuffer</a> failed to retrieve a data buffer and *<i>ppData</i> points to <b>NULL</b>. For more information, see Remarks.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_BUFFER_TOO_LARGE</b></dt>
</dl>
</td>
<td width="60%">
The <i>NumFramesRequested</i> value exceeds the available buffer space (buffer size minus padding size).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_BUFFER_SIZE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The stream is exclusive mode and uses event-driven buffering, but the client attempted to get a packet that was not the size of the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
A previous <b>IAudioRenderClient::GetBuffer</b> call is still in effect.

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
<dt><b>AUDCLNT_E_RESOURCES_INVALIDATED</b></dt>
</dl>
</td>
<td width="60%">
The stream's resources have been invalidated. This error may be thrown for the following reasons:<br>
- The stream is suspended.<br>
- An Exclusive or Offload stream is disconnected.<br>
- A packaged application that has an exclusive mode or offload stream is quiesced.<br>
- A "protected output" stream is closed.<br>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_BUFFER_OPERATION_PENDING</b></dt>
</dl>
</td>
<td width="60%">
Buffer cannot be accessed because a stream reset is in progress.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>ppData</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

The caller can request a packet size that is less than or equal to the amount of available space in the buffer (except in the case of an exclusive-mode stream that uses event-driven buffering; for more information, see <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>). The available space is simply the buffer size minus the amount of data in the buffer that is already queued up to be played. If the caller specifies a <i>NumFramesRequested</i> value that exceeds the available space in the buffer, the call fails and returns error code AUDCLNT_E_BUFFER_TOO_LARGE.

The client is responsible for writing a sufficient amount of data to the buffer to prevent glitches from occurring in the audio stream. For more information about buffering requirements, see <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>.

After obtaining a data packet by calling <b>GetBuffer</b>, the client fills the packet with rendering data and issues the packet to the audio engine by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-releasebuffer">IAudioRenderClient::ReleaseBuffer</a> method.

The client must call <b>ReleaseBuffer</b> after a <b>GetBuffer</b> call that successfully obtains a packet of any size other than 0. The client has the option of calling or not calling <b>ReleaseBuffer</b> to release a packet of size 0.

For nonzero packet sizes, the client must alternate calls to <b>GetBuffer</b> and <b>ReleaseBuffer</b>. Each <b>GetBuffer</b> call must be followed by a corresponding <b>ReleaseBuffer</b> call. After the client has called <b>GetBuffer</b> to acquire a data packet, the client cannot acquire the next data packet until it has called <b>ReleaseBuffer</b> to release the previous packet. Two or more consecutive calls either to <b>GetBuffer</b> or to <b>ReleaseBuffer</b> are not permitted and will fail with error code AUDCLNT_E_OUT_OF_ORDER.

To ensure the correct ordering of calls, a <b>GetBuffer</b> call and its corresponding <b>ReleaseBuffer</b> call must occur in the same thread.

The size of an audio frame is specified by the <b>nBlockAlign</b> member of the <b>WAVEFORMATEX</b> structure that the client obtains by calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getmixformat">IAudioClient::GetMixFormat</a> method.

If the caller sets <i>NumFramesRequested</i> = 0, the method returns status code S_OK but does not write to the variable that the <i>ppData</i> parameter points to.

Clients should avoid excessive delays between the <b>GetBuffer</b> call that acquires a buffer and the <b>ReleaseBuffer</b> call that releases the buffer. The implementation of the audio engine assumes that the <b>GetBuffer</b> call and the corresponding <b>ReleaseBuffer</b> call occur within the same buffer-processing period. Clients that delay releasing a buffer for more than one period risk losing sample data.

In Windows 7, <b>GetBuffer</b> can return the <b>AUDCLNT_E_BUFFER_ERROR</b> error code for an audio client that uses the endpoint buffer in the exclusive mode. This error indicates that the data buffer was not retrieved because a data packet was not available (*<i>ppData</i> received <b>NULL</b>).   

If <b>GetBuffer</b> returns <b>AUDCLNT_E_BUFFER_ERROR</b>, the thread consuming the audio samples must wait for the next processing pass. The client might benefit from keeping a count of the failed <b>GetBuffer</b> calls. If <b>GetBuffer</b> returns this error repeatedly, the client can start a new processing loop after shutting down the current client by calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-stop">IAudioClient::Stop</a>, <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-reset">IAudioClient::Reset</a>, and releasing the audio client.


#### Examples

For code examples that call the <b>GetBuffer</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/exclusive-mode-streams">Exclusive-Mode Streams</a>
</li>
</ul>
<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getbuffersize">IAudioClient::GetBufferSize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getcurrentpadding">IAudioClient::GetCurrentPadding</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiorenderclient">IAudioRenderClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-releasebuffer">IAudioRenderClient::ReleaseBuffer</a>