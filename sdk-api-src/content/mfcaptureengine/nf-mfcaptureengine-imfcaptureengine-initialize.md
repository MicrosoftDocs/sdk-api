---
UID: NF:mfcaptureengine.IMFCaptureEngine.Initialize
title: IMFCaptureEngine::Initialize (mfcaptureengine.h)
description: Initializes the capture engine.
helpviewer_keywords: ["IMFCaptureEngine interface [Media Foundation]","Initialize method","IMFCaptureEngine.Initialize","IMFCaptureEngine::Initialize","Initialize","Initialize method [Media Foundation]","Initialize method [Media Foundation]","IMFCaptureEngine interface","mf.imfcaptureengine_initialize","mfcaptureengine/IMFCaptureEngine::Initialize"]
old-location: mf\imfcaptureengine_initialize.htm
tech.root: mf
ms.assetid: 23EC8B49-2F67-4FB8-AFFA-409823ACCF59
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],Initialize method, IMFCaptureEngine.Initialize, IMFCaptureEngine::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_initialize, mfcaptureengine/IMFCaptureEngine::Initialize
req.header: mfcaptureengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFCaptureEngine::Initialize
 - mfcaptureengine/IMFCaptureEngine::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngine.Initialize
---

# IMFCaptureEngine::Initialize


## -description

Initializes the capture engine.

## -parameters

### -param pEventCallback [in]

A pointer to the <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineoneventcallback">IMFCaptureEngineOnEventCallback</a> interface. The caller must implement this interface. The capture engine uses this interface to send asynchronous events to the caller.

### -param pAttributes [in, optional]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface. This parameter can be <b>NULL</b>. 

You can use this parameter to configure the capture engine. Call <a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes">MFCreateAttributes</a> to create an attribute store, and then set any of the following attributes.

<ul>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-d3d-manager">MF_CAPTURE_ENGINE_D3D_MANAGER</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-disable-dxva">MF_CAPTURE_ENGINE_DISABLE_DXVA</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-disable-hardware-transforms">MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-encoder-mft-fieldofuse-unlock-attribute">MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-event-generator-guid">MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/legacy/hh162817(v=vs.85)">MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-mediasource-config">MF_CAPTURE_ENGINE_MEDIASOURCE_CONFIG</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-record-sink-audio-max-processed-samples">MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-record-sink-audio-max-unprocessed-samples">MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-record-sink-video-max-processed-samples">MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-record-sink-video-max-unprocessed-samples">MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-use-audio-device-only">MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY</a>
</li>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-use-video-device-only">MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY</a>
</li>
</ul>

### -param pAudioSource [in, optional]

An <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer that specifies an audio-capture device. This parameter can be <b>NULL</b>.

If you set the <a href="/windows/desktop/medfound/mf-capture-engine-use-video-device-only">MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY</a> attribute to <b>TRUE</b> in <i>pAttributes</i>, the capture engine does not use an audio device, and the <i>pAudioSource</i> parameter is ignored.

Otherwise, if <i>pAudioSource</i> is <b>NULL</b>, the capture engine selects the microphone that is built into the video camera specified by <i>pVideoSource</i>. If the video camera does not have a microphone, the capture engine enumerates the audio-capture devices on the system and selects the first one.

To override the default audio device, set <i>pAudioSource</i> to an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> or <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer for the device. For more information, see <a href="/windows/desktop/medfound/audio-video-capture-in-media-foundation">Audio/Video Capture in Media Foundation</a>.

### -param pVideoSource [in, optional]

An <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer that specifies a video-capture device. This parameter can be <b>NULL</b>.

If you set the <a href="/windows/desktop/medfound/mf-capture-engine-use-audio-device-only">MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY</a> attribute to <b>TRUE</b> in <i>pAttributes</i>, the capture engine does not use a video device, and the <i>pVideoSource</i> parameter is ignored.

Otherwise, if <i>pVideoSource</i> is <b>NULL</b>, the capture engine enumerates the video-capture devices on the system and selects the first one.

To override the default video device, set <i>pVideoSource</i> to an <a href="/windows/desktop/api/mfidl/nn-mfidl-imfmediasource">IMFMediaSource</a> or <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate">IMFActivate</a> pointer for the device. For more information, see <a href="/windows/desktop/medfound/enumerating-video-capture-devices">Enumerating Video Capture Devices</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize">Initialize</a> method was already called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_CAPTURE_DEVICES_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No capture devices are available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_CAPTURE_DEVICE_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
An unsupported capture device is present on the system. This error will only be returned if NULL is specified for the <i>pVideoSource</i> parameter, indicating that the system should pick the capture device, and if no supported capture device has already been attached. It is recommended that apps show users a specific unsupported capture device message if this error is returned, rather than a general failure message.

</td>
</tr>
</table>

## -remarks

You must call this method once before using the capture engine. Calling the method a second time returns <b>MF_E_INVALIDREQUEST</b>.

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_INITIALIZED</b> event through the <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengineoneventcallback-onevent">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a>