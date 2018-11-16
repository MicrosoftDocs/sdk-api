---
UID: NF:mfcaptureengine.IMFCaptureEngineOnEventCallback.OnEvent
title: IMFCaptureEngineOnEventCallback::OnEvent
author: windows-sdk-content
description: Called by the capture engine to notify the application of a capture event.
old-location: mf\imfcaptureengineoneventcallback_onevent.htm
tech.root: medfound
ms.assetid: 26C5B2E5-0543-49FC-915A-DCE097FF66BA
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IMFCaptureEngineOnEventCallback interface [Media Foundation],OnEvent method, IMFCaptureEngineOnEventCallback.OnEvent, IMFCaptureEngineOnEventCallback::OnEvent, OnEvent, OnEvent method [Media Foundation], OnEvent method [Media Foundation],IMFCaptureEngineOnEventCallback interface, mf.imfcaptureengineoneventcallback_onevent, mfcaptureengine/IMFCaptureEngineOnEventCallback::OnEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngineOnEventCallback.OnEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mfcaptureengine.h
: 
- IMFCaptureEngineOnEventCallback.OnEvent
: 
---

# IMFCaptureEngineOnEventCallback::OnEvent


## -description


Called by the capture engine to notify the application of a capture event.


## -parameters




### -param pEvent [in]

A pointer to the <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> interface. Use this interface to get information about the event, as described in Remarks.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To get the type of event, call <a href="https://msdn.microsoft.com/56284491-6f84-467e-9fac-46b04db4024a">IMFMediaEvent::GetExtendedType</a>. This method returns one of the following GUIDs.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_ALL_EFFECTS_REMOVED</b></td>
<td>The <a href="https://msdn.microsoft.com/C01F7A61-3585-4E8B-B914-7DB1446D1BC1">IMFCaptureSource::RemoveAllEffects</a> method completed.</td>
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
<td>The <a href="https://msdn.microsoft.com/C108360D-0B8C-4539-9D78-A5559100086E">IMFCaptureSource::AddEffect</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_EFFECT_REMOVED</b></td>
<td>The <a href="https://msdn.microsoft.com/5FF2EF1C-1BF0-4CF7-95AB-1BB10025D66F">IMFCaptureSource::RemoveEffect</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_ERROR</b></td>
<td>An error occurred during capture.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_INITIALIZED</b></td>
<td>The <a href="https://msdn.microsoft.com/23EC8B49-2F67-4FB8-AFFA-409823ACCF59">IMFCaptureEngine::Initialize</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_PHOTO_TAKEN</b></td>
<td>The <a href="https://msdn.microsoft.com/6E633E90-9C8B-44B6-9149-704872143147">IMFCaptureEngine::TakePhoto</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_PREVIEW_STARTED</b></td>
<td>The <a href="https://msdn.microsoft.com/C5BCF990-E7F9-48E9-B082-79953F5ED27C">IMFCaptureEngine::StartPreview</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_PREVIEW_STOPPED</b></td>
<td>The <a href="https://msdn.microsoft.com/36DE5079-D4D5-4FC5-8CF6-1F5B3F9E8B66">IMFCaptureEngine::StopPreview</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_RECORD_STARTED</b></td>
<td>The <a href="https://msdn.microsoft.com/22084409-B2E6-47EF-A59B-A762E9A9191D">IMFCaptureEngine::StartRecord</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_ENGINE_RECORD_STOPPED</b></td>
<td>The <a href="https://msdn.microsoft.com/737C23E0-D4EF-4630-A460-2AE56FE50A12">IMFCaptureEngine::StopRecord</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_SINK_PREPARED</b></td>
<td>The <a href="https://msdn.microsoft.com/244FD291-AD1D-4A51-87C3-C98B33978AA1">IMFCaptureSink::Prepare</a> method completed.</td>
</tr>
<tr>
<td><b>MF_CAPTURE_SOURCE_CURRENT_DEVICE_MEDIA_TYPE_SET</b></td>
<td>The <a href="https://msdn.microsoft.com/2B88BBAE-E837-4F4A-B697-64772F25C89D">IMFCaptureSource::SetCurrentDeviceMediaType</a>   method completed.</td>
</tr>
</table>
 

This method may be called from a worker thread. The implementation should be thread-safe.

To get the status code for the event, call <a href="https://msdn.microsoft.com/e2fc6c81-11c0-4947-b647-3e74a73ee5a2">IMFMediaEvent::GetStatus</a>. If the status code is an error code, it indicates that the requested operation failed.

In addition, the event object specified by <i>pEvent</i> might contain any of the following attributes.

<ul>
<li>
<a href="https://msdn.microsoft.com/DCCF3054-AF14-44C7-84C0-B03E35B5D90A">MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A15B334A-716A-467E-AEA5-C13710FFE109">MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX</a>
</li>
</ul>
To get event attributes, use the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface, which <a href="https://msdn.microsoft.com/b4f686be-9472-433c-b983-6c48dfd3ac76">IMFMediaEvent</a> inherits.




## -see-also




<a href="https://msdn.microsoft.com/6F04F843-160C-4F49-9841-ECC1450F4A58">IMFCaptureEngineOnEventCallback</a>
 

 

