---
UID: NF:mfcaptureengine.IMFCaptureEngine.Initialize
title: IMFCaptureEngine::Initialize
author: windows-sdk-content
description: Initializes the capture engine.
old-location: mf\imfcaptureengine_initialize.htm
old-project: medfound
ms.assetid: 23EC8B49-2F67-4FB8-AFFA-409823ACCF59
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: IMFCaptureEngine interface [Media Foundation],Initialize method, IMFCaptureEngine.Initialize, IMFCaptureEngine::Initialize, Initialize, Initialize method [Media Foundation], Initialize method [Media Foundation],IMFCaptureEngine interface, mf.imfcaptureengine_initialize, mfcaptureengine/IMFCaptureEngine::Initialize
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngine.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureEngine::Initialize


## -description


Initializes the capture engine.


## -parameters




### -param pEventCallback [in]

A pointer to the <a href="https://msdn.microsoft.com/6F04F843-160C-4F49-9841-ECC1450F4A58">IMFCaptureEngineOnEventCallback</a> interface. The caller must implement this interface. The capture engine uses this interface to send asynchronous events to the caller.


### -param pAttributes [in, optional]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface. This parameter can be <b>NULL</b>. 

You can use this parameter to configure the capture engine. Call <a href="https://msdn.microsoft.com/a79b1edd-5ca1-4550-a6ce-58073155affd">MFCreateAttributes</a> to create an attribute store, and then set any of the following attributes.

<ul>
<li>
<a href="https://msdn.microsoft.com/1DFDE7AB-7DFF-4C39-9460-E42E37649AAC">MF_CAPTURE_ENGINE_D3D_MANAGER</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9F677E6E-0DCD-456F-8A00-1C11011BAA13">MF_CAPTURE_ENGINE_DISABLE_DXVA</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1C687FEC-276D-4759-A3B8-9A2A31CB0DE1">MF_CAPTURE_ENGINE_DISABLE_HARDWARE_TRANSFORMS</a>
</li>
<li>
<a href="https://msdn.microsoft.com/28421875-9629-4F14-8159-2D86012F517F">MF_CAPTURE_ENGINE_ENCODER_MFT_FIELDOFUSE_UNLOCK_Attribute</a>
</li>
<li>
<a href="https://msdn.microsoft.com/DCCF3054-AF14-44C7-84C0-B03E35B5D90A">MF_CAPTURE_ENGINE_EVENT_GENERATOR_GUID</a>
</li>
<li>
<a href="https://msdn.microsoft.com/A15B334A-716A-467E-AEA5-C13710FFE109">MF_CAPTURE_ENGINE_EVENT_STREAM_INDEX</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9A21D21B-E77F-4C7C-B41F-361CEDA322E7">MF_CAPTURE_ENGINE_MEDIASOURCE_CONFIG</a>
</li>
<li>
<a href="https://msdn.microsoft.com/216886DB-B206-4944-925A-C2106331F1CB">MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_PROCESSED_SAMPLES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/C959ED58-77EB-47EC-8D5D-BBFA9342295D">MF_CAPTURE_ENGINE_RECORD_SINK_AUDIO_MAX_UNPROCESSED_SAMPLES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/5AFA197E-5A7F-402E-A62B-4F624A5DD917">MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_PROCESSED_SAMPLES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/B3B5C547-1F06-45B1-BFCB-513AD7B6A9B6">MF_CAPTURE_ENGINE_RECORD_SINK_VIDEO_MAX_UNPROCESSED_SAMPLES</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0A905D55-CEE5-44FC-97A5-9474872D5724">MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY</a>
</li>
<li>
<a href="https://msdn.microsoft.com/B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29">MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY</a>
</li>
</ul>

### -param pAudioSource [in, optional]

An <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer that specifies an audio-capture device. This parameter can be <b>NULL</b>.

If you set the <a href="https://msdn.microsoft.com/B0B7A7F2-02F9-46A6-954F-D6E9C3B73A29">MF_CAPTURE_ENGINE_USE_VIDEO_DEVICE_ONLY</a> attribute to <b>TRUE</b> in <i>pAttributes</i>, the capture engine does not use an audio device, and the <i>pAudioSource</i> parameter is ignored.

Otherwise, if <i>pAudioSource</i> is <b>NULL</b>, the capture engine selects the microphone that is built into the video camera specified by <i>pVideoSource</i>. If the video camera does not have a microphone, the capture engine enumerates the audio-capture devices on the system and selects the first one.

To override the default audio device, set <i>pAudioSource</i> to an <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> or <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointer for the device. For more information, see <a href="https://msdn.microsoft.com/8a9d96f8-1096-4b66-a2ec-8a95d754ea72">Audio/Video Capture in Media Foundation</a>.


### -param pVideoSource [in, optional]

An <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> pointer that specifies a video-capture device. This parameter can be <b>NULL</b>.

If you set the <a href="https://msdn.microsoft.com/0A905D55-CEE5-44FC-97A5-9474872D5724">MF_CAPTURE_ENGINE_USE_AUDIO_DEVICE_ONLY</a> attribute to <b>TRUE</b> in <i>pAttributes</i>, the capture engine does not use a video device, and the <i>pVideoSource</i> parameter is ignored.

Otherwise, if <i>pVideoSource</i> is <b>NULL</b>, the capture engine enumerates the video-capture devices on the system and selects the first one.

To override the default video device, set <i>pVideoSource</i> to an <a href="https://msdn.microsoft.com/8b579f61-6fea-4b20-a051-7633fc01fa05">IMFMediaSource</a> or <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> pointer for the device. For more information, see <a href="https://msdn.microsoft.com/b1267478-329b-4e46-a2ed-1ec11d2e2e6d">Enumerating Video Capture Devices</a>.


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
The <a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a> method was already called.

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
</table>
 




## -remarks



You must call this method once before using the capture engine. Calling the method a second time returns <b>MF_E_INVALIDREQUEST</b>.

This method is asynchronous. If the method returns a success code, the caller will receive an <b>MF_CAPTURE_ENGINE_INITIALIZED</b> event through the <a href="https://msdn.microsoft.com/26C5B2E5-0543-49FC-915A-DCE097FF66BA">IMFCaptureEngineOnEventCallback::OnEvent</a> method. The operation can fail asynchronously after the method succeeds. If so, the error code is conveyed through the <b>OnEvent</b> method.




## -see-also




<a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a>
 

 

