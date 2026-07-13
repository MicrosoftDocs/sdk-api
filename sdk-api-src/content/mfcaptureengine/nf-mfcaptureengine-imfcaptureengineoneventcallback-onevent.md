---
UID: NF:mfcaptureengine.IMFCaptureEngineOnEventCallback.OnEvent
title: IMFCaptureEngineOnEventCallback::OnEvent (mfcaptureengine.h)
description: Called by the capture engine to notify the application of a capture event.
helpviewer_keywords: ["IMFCaptureEngineOnEventCallback interface [Media Foundation]","OnEvent method","IMFCaptureEngineOnEventCallback.OnEvent","IMFCaptureEngineOnEventCallback::OnEvent","OnEvent","OnEvent method [Media Foundation]","OnEvent method [Media Foundation]","IMFCaptureEngineOnEventCallback interface","mf.imfcaptureengineoneventcallback_onevent","mfcaptureengine/IMFCaptureEngineOnEventCallback::OnEvent"]
old-location: mf\imfcaptureengineoneventcallback_onevent.htm
tech.root: mf
ms.assetid: 26C5B2E5-0543-49FC-915A-DCE097FF66BA
ms.date: 12/05/2018
ms.keywords: IMFCaptureEngineOnEventCallback interface [Media Foundation],OnEvent method, IMFCaptureEngineOnEventCallback.OnEvent, IMFCaptureEngineOnEventCallback::OnEvent, OnEvent, OnEvent method [Media Foundation], OnEvent method [Media Foundation],IMFCaptureEngineOnEventCallback interface, mf.imfcaptureengineoneventcallback_onevent, mfcaptureengine/IMFCaptureEngineOnEventCallback::OnEvent
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
 - IMFCaptureEngineOnEventCallback::OnEvent
 - mfcaptureengine/IMFCaptureEngineOnEventCallback::OnEvent
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
 - IMFCaptureEngineOnEventCallback.OnEvent
---

# IMFCaptureEngineOnEventCallback::OnEvent


## -description

Called by the capture engine to notify the application of a capture event.

## -parameters

### -param pEvent [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface. Use this interface to get information about the event, as described in Remarks.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To get the type of event, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getextendedtype">IMFMediaEvent::GetExtendedType</a>. This method returns one of the following GUIDs.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_ALL_EFFECTS_REMOVED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-removealleffects">IMFCaptureSource::RemoveAllEffects</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_CAMERA_STREAM_BLOCKED</b></td>
<td>Video capture has been blocked by the driver.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_CAMERA_STREAM_UNBLOCKED</b></td>
<td>Video capture has been restored by the driver after having been blocked.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_EFFECT_ADDED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-addeffect">IMFCaptureSource::AddEffect</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_EFFECT_REMOVED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-removeeffect">IMFCaptureSource::RemoveEffect</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_ERROR</b></td>
<td>An error occurred during capture.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_INITIALIZED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-initialize">IMFCaptureEngine::Initialize</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_PHOTO_TAKEN</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-takephoto">IMFCaptureEngine::TakePhoto</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_PREVIEW_STARTED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startpreview">IMFCaptureEngine::StartPreview</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_PREVIEW_STOPPED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-stoppreview">IMFCaptureEngine::StopPreview</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_RECORD_STARTED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-startrecord">IMFCaptureEngine::StartRecord</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_RECORD_STOPPED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcaptureengine-stoprecord">IMFCaptureEngine::StopRecord</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_SINK_PREPARED</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesink-prepare">IMFCaptureSink::Prepare</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_SOURCE_CURRENT_DEVICE_MEDIA_TYPE_SET</b></td>
<td>The <a href="/windows/desktop/api/mfcaptureengine/nf-mfcaptureengine-imfcapturesource-setcurrentdevicemediatype">IMFCaptureSource::SetCurrentDeviceMediaType</a>   method completed.</td>
</tr>
</table>
 

This method may be called from a worker thread. The implementation should be thread-safe.

To get the status code for the event, call <a href="/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getstatus">IMFMediaEvent::GetStatus</a>. If the status code is an error code, it indicates that the requested operation failed.

In addition, the event object specified by <i>pEvent</i> might contain any of the following attributes.

<ul>
<li>
<a href="/windows/desktop/medfound/mf-capture-engine-event-generator-guid">MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID</a>
</li>
<li>
<a href="/previous-versions/windows/desktop/legacy/hh162817(v=vs.85)">MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX</a>
</li>
</ul>
To get event attributes, use the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface, which <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> inherits.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineoneventcallback">IMFCaptureEngineOnEventCallback</a>