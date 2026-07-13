---
UID: NF:audioclient.IAudioClient.GetCurrentPadding
title: IAudioClient::GetCurrentPadding (audioclient.h)
description: The GetCurrentPadding method retrieves the number of frames of padding in the endpoint buffer.
helpviewer_keywords: ["GetCurrentPadding","GetCurrentPadding method [Core Audio]","GetCurrentPadding method [Core Audio]","IAudioClient interface","IAudioClient interface [Core Audio]","GetCurrentPadding method","IAudioClient.GetCurrentPadding","IAudioClient::GetCurrentPadding","IAudioClientGetCurrentPadding","audioclient/IAudioClient::GetCurrentPadding","coreaudio.iaudioclient_getcurrentpadding"]
old-location: coreaudio\iaudioclient_getcurrentpadding.htm
tech.root: CoreAudio
ms.assetid: 2a2c9ddf-f668-41ff-85f0-34de593c0fe2
ms.date: 12/05/2018
ms.keywords: GetCurrentPadding, GetCurrentPadding method [Core Audio], GetCurrentPadding method [Core Audio],IAudioClient interface, IAudioClient interface [Core Audio],GetCurrentPadding method, IAudioClient.GetCurrentPadding, IAudioClient::GetCurrentPadding, IAudioClientGetCurrentPadding, audioclient/IAudioClient::GetCurrentPadding, coreaudio.iaudioclient_getcurrentpadding
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
 - IAudioClient::GetCurrentPadding
 - audioclient/IAudioClient::GetCurrentPadding
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
 - IAudioClient.GetCurrentPadding
---

# IAudioClient::GetCurrentPadding


## -description

The <b>GetCurrentPadding</b> method retrieves the number of frames of padding in the endpoint buffer.

## -parameters

### -param pNumPaddingFrames [out]

Pointer to a <b>UINT32</b> variable into which the method writes the frame count (the number of audio frames of padding in the buffer).

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
Parameter <i>pNumPaddingFrames</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method requires prior initialization of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

This method retrieves a padding value that indicates the amount of valid, unread data that the endpoint buffer currently contains. A rendering application can use the padding value to determine how much new data it can safely write to the endpoint buffer without overwriting previously written data that the audio engine has not yet read from the buffer. A capture application can use the padding value to determine how much new data it can safely read from the endpoint buffer without reading invalid data from a region of the buffer to which the audio engine has not yet written valid data.

The padding value is expressed as a number of audio frames. The size of an audio frame is specified by the <b>nBlockAlign</b> member of the <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> (or <a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-waveformatextensible">WAVEFORMATEXTENSIBLE</a>) structure that the client passed to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>  method. The size in bytes of an audio frame equals the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples.

For a shared-mode rendering stream, the padding value reported by <b>GetCurrentPadding</b> specifies the number of audio frames that are queued up to play in the endpoint buffer. Before writing to the endpoint buffer, the client can calculate the amount of available space in the buffer by subtracting the padding value from the buffer length. To ensure that a subsequent call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a> method succeeds, the client should request a packet length that does not exceed the available space in the buffer. To obtain the buffer length, call the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-getbuffersize">IAudioClient::GetBufferSize</a> method.

For a shared-mode capture stream, the padding value reported by <b>GetCurrentPadding</b> specifies the number of frames of capture data that are available in the next packet in the endpoint buffer. At a particular moment, zero, one, or more packets of capture data might be ready for the client to read from the buffer. If no packets are currently available, the method reports a padding value of 0. Following the <b>GetCurrentPadding</b> call, an <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a> method call will retrieve a packet whose length exactly equals the padding value reported by <b>GetCurrentPadding</b>. Each call to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">GetBuffer</a> retrieves a whole packet. A packet always contains an integral number of audio frames.

For a shared-mode capture stream, calling <b>GetCurrentPadding</b> is equivalent to calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize">IAudioCaptureClient::GetNextPacketSize</a> method. That is, the padding value reported by <b>GetCurrentPadding</b> is equal to the packet length reported by <b>GetNextPacketSize</b>.

For an exclusive-mode rendering or capture stream that was initialized with the AUDCLNT_STREAMFLAGS_EVENTCALLBACK flag, the client typically has no use for the padding value reported by <b>GetCurrentPadding</b>. Instead, the client accesses an entire buffer during each processing pass. Each time a buffer becomes available for processing, the audio engine notifies the client by signaling the client's event handle. For more information about this flag, see <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>.

For an exclusive-mode rendering or capture stream that was not initialized with the AUDCLNT_STREAMFLAGS_EVENTCALLBACK flag, the client can use the padding value obtained from <b>GetCurrentPadding</b> in a way that is similar to that described previously for a shared-mode stream. The details are as follows.

First, for an exclusive-mode rendering stream, the padding value specifies the number of audio frames that are queued up to play in the endpoint buffer. As before, the client can calculate the amount of available space in the buffer by subtracting the padding value from the buffer length.

Second, for an exclusive-mode capture stream, the padding value reported by <b>GetCurrentPadding</b> specifies the current length of the next packet. However, this padding value is a snapshot of the packet length, which might increase before the client calls the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a> method. Thus, the length of the packet retrieved by <b>GetBuffer</b> is at least as large as, but might be larger than, the padding value reported by the <b>GetCurrentPadding</b> call that preceded the <b>GetBuffer</b> call. In contrast, for a shared-mode capture stream, the length of the packet obtained from <b>GetBuffer</b> always equals the padding value reported by the preceding <b>GetCurrentPadding</b> call.

For a code example that calls the <b>GetCurrentPadding</b> method, see <a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>.

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getbuffer">IAudioCaptureClient::GetBuffer</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiocaptureclient-getnextpacketsize">IAudioCaptureClient::GetNextPacketSize</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a>