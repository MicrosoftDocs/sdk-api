---
UID: NF:audioclient.IAudioClient.GetBufferSize
title: IAudioClient::GetBufferSize (audioclient.h)
description: The GetBufferSize method retrieves the size (maximum capacity) of the endpoint buffer.
helpviewer_keywords: ["GetBufferSize","GetBufferSize method [Core Audio]","GetBufferSize method [Core Audio]","IAudioClient interface","IAudioClient interface [Core Audio]","GetBufferSize method","IAudioClient.GetBufferSize","IAudioClient::GetBufferSize","IAudioClientGetBufferSize","audioclient/IAudioClient::GetBufferSize","coreaudio.iaudioclient_getbuffersize"]
old-location: coreaudio\iaudioclient_getbuffersize.htm
tech.root: CoreAudio
ms.assetid: 562d2db6-ae14-47c9-8b8f-d4d90072b3dd
ms.date: 12/05/2018
ms.keywords: GetBufferSize, GetBufferSize method [Core Audio], GetBufferSize method [Core Audio],IAudioClient interface, IAudioClient interface [Core Audio],GetBufferSize method, IAudioClient.GetBufferSize, IAudioClient::GetBufferSize, IAudioClientGetBufferSize, audioclient/IAudioClient::GetBufferSize, coreaudio.iaudioclient_getbuffersize
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
 - IAudioClient::GetBufferSize
 - audioclient/IAudioClient::GetBufferSize
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
 - IAudioClient.GetBufferSize
---

# IAudioClient::GetBufferSize


## -description

The <b>GetBufferSize</b> method retrieves the size (maximum capacity) of the endpoint buffer.

## -parameters

### -param pNumBufferFrames [out]

Pointer to a <b>UINT32</b> variable into which the method writes the number of audio frames that the buffer can hold.

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
Parameter <i>pNumBufferFrames</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -remarks

This method requires prior initialization of the <a href="/windows/desktop/api/audioclient/nn-audioclient-iaudioclient">IAudioClient</a> interface. All calls to this method will fail with the error AUDCLNT_E_NOT_INITIALIZED until the client initializes the audio stream by successfully calling the <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method.

This method retrieves the length of the endpoint buffer shared between the client application and the audio engine. The length is expressed as the number of audio frames the buffer can hold. The size in bytes of an audio frame is calculated as the number of channels in the stream multiplied by the sample size per channel. For example, the frame size is four bytes for a stereo (2-channel) stream with 16-bit samples.

The <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudioclient-initialize">IAudioClient::Initialize</a> method allocates the buffer. The client specifies the buffer length in the <i>hnsBufferDuration</i> parameter value that it passes to the <b>Initialize</b> method. For rendering clients, the buffer length determines the maximum amount of rendering data that the application can write to the endpoint buffer during a single processing pass. For capture clients, the buffer length determines the maximum amount of capture data that the audio engine can read from the endpoint buffer during a single processing pass. The client should always call <b>GetBufferSize</b> after calling <b>Initialize</b> to determine the actual size of the allocated buffer, which might differ from the requested size.

Rendering clients can use this value to calculate the largest rendering buffer size that can be requested from <a href="/windows/desktop/api/audioclient/nf-audioclient-iaudiorenderclient-getbuffer">IAudioRenderClient::GetBuffer</a> during each processing pass.

For code examples that call the <b>GetBufferSize</b> method, see the following topics:

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