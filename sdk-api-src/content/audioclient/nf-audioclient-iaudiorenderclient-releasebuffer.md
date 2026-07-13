---
UID: NF:audioclient.IAudioRenderClient.ReleaseBuffer
title: IAudioRenderClient::ReleaseBuffer (audioclient.h)
description: The ReleaseBuffer method releases the buffer space acquired in the previous call to the IAudioRenderClient::GetBuffer method.
helpviewer_keywords: ["IAudioRenderClient interface [Core Audio]","ReleaseBuffer method","IAudioRenderClient.ReleaseBuffer","IAudioRenderClient::ReleaseBuffer","IAudioRenderClientReleaseBuffer","ReleaseBuffer","ReleaseBuffer method [Core Audio]","ReleaseBuffer method [Core Audio]","IAudioRenderClient interface","audioclient/IAudioRenderClient::ReleaseBuffer","coreaudio.iaudiorenderclient_releasebuffer"]
old-location: coreaudio\iaudiorenderclient_releasebuffer.htm
tech.root: CoreAudio
ms.assetid: 19d89b5e-2e73-4693-b970-7ebf452ef9a1
ms.date: 12/05/2018
ms.keywords: IAudioRenderClient interface [Core Audio],ReleaseBuffer method, IAudioRenderClient.ReleaseBuffer, IAudioRenderClient::ReleaseBuffer, IAudioRenderClientReleaseBuffer, ReleaseBuffer, ReleaseBuffer method [Core Audio], ReleaseBuffer method [Core Audio],IAudioRenderClient interface, audioclient/IAudioRenderClient::ReleaseBuffer, coreaudio.iaudiorenderclient_releasebuffer
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
 - IAudioRenderClient::ReleaseBuffer
 - audioclient/IAudioRenderClient::ReleaseBuffer
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
 - IAudioRenderClient.ReleaseBuffer
---

# IAudioRenderClient::ReleaseBuffer


## -description

The <b>ReleaseBuffer</b> method releases the buffer space acquired in the previous call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a> method.

## -parameters

### -param NumFramesWritten [in]

The number of audio frames written by the client to the data packet. The value of this parameter must be less than or equal to the size of the data packet, as specified in the <i>NumFramesRequested</i> parameter passed to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a> method.

### -param dwFlags [in]

The buffer-configuration flags. The caller can set this parameter either to 0 or to the following <a href="/windows/win32/api/audioclient/ne-audioclient-_audclnt_bufferflags">_AUDCLNT_BUFFERFLAGS</a> enumeration value (a flag bit):

AUDCLNT_BUFFERFLAGS_SILENT

If this flag bit is set, the audio engine treats the data packet as though it contains silence regardless of the data values contained in the packet. This flag eliminates the need for the client to explicitly write silence data to the rendering buffer.

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
<dt><b>AUDCLNT_E_INVALID_SIZE</b></dt>
</dl>
</td>
<td width="60%">
The <i>NumFramesWritten</i> value exceeds the <i>NumFramesRequested</i> value specified in the previous <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a> call.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_BUFFER_SIZE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The stream is exclusive mode and uses event-driven buffering, but the client attempted to release a packet that was not the size of the buffer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>AUDCLNT_E_OUT_OF_ORDER</b></dt>
</dl>
</td>
<td width="60%">
This call was not preceded by a corresponding call to <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a>.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Parameter <i>dwFlags</i> is not a valid value.<br>

</td>
</tr>
</table>

## -remarks

The client must release the same number of frames that it requested in the preceding call to the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a> method. The single exception to this rule is that the client can always call <b>ReleaseBuffer</b> to release 0 frames (unless the stream is exclusive mode and uses event-driven buffering).

This behavior provides a convenient means for the client to "release" a previously requested packet of length 0. In this case, the call to <b>ReleaseBuffer</b> is optional. After calling <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">GetBuffer</a> to obtain a packet of length 0, the client has the option of not calling <b>ReleaseBuffer</b> before calling <b>GetBuffer</b> again.

In addition, if the preceding <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">GetBuffer</a> call obtained a packet of nonzero size, calling <b>ReleaseBuffer</b> with <i>NumFramesRequested</i> set to 0 will succeed (unless the stream is exclusive mode and uses event-driven buffering). The meaning of the call is that the client wrote no data to the packet before releasing it. Thus, the method treats the portion of the buffer represented by the packet as unused and will make this portion of the buffer available again to the client in the next <b>GetBuffer</b> call.

Clients should avoid excessive delays between the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">GetBuffer</a> call that acquires a buffer and the <b>ReleaseBuffer</b> call that releases the buffer. The implementation of the audio engine assumes that the <b>GetBuffer</b> call and the corresponding <b>ReleaseBuffer</b> call occur within the same buffer-processing period. Clients that delay releasing a buffer for more than one period risk losing sample data.

For code examples that call the <b>ReleaseBuffer</b> method, see the following topics:

<ul>
<li>
<a href="/windows/desktop/CoreAudio/rendering-a-stream">Rendering a Stream</a>
</li>
<li>
<a href="/windows/desktop/CoreAudio/exclusive-mode-streams">Exclusive-Mode Streams</a>
</li>
</ul>

## -see-also

<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a>



<a href="/windows/desktop/api/audioclient/nn-audioclient-iaudiorenderclient">IAudioRenderClient Interface</a>



<a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a>