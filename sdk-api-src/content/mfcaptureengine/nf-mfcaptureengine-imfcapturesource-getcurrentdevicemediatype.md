---
UID: NF:mfcaptureengine.IMFCaptureSource.GetCurrentDeviceMediaType
title: IMFCaptureSource::GetCurrentDeviceMediaType
author: windows-sdk-content
description: Gets the current media type for a capture stream.
old-location: mf\imfcapturesource_getcurrentdevicemediatype.htm
tech.root: medfound
ms.assetid: 8F263F5C-D1B4-4DF7-AFCB-E27575FBAAA2
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: GetCurrentDeviceMediaType, GetCurrentDeviceMediaType method [Media Foundation], GetCurrentDeviceMediaType method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetCurrentDeviceMediaType method, IMFCaptureSource.GetCurrentDeviceMediaType, IMFCaptureSource::GetCurrentDeviceMediaType, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, mf.imfcapturesource_getcurrentdevicemediatype, mfcaptureengine/IMFCaptureSource::GetCurrentDeviceMediaType
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
 - IMFCaptureSource.GetCurrentDeviceMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource::GetCurrentDeviceMediaType


## -description


Gets the current media type for a capture stream.


## -parameters




### -param dwSourceStreamIndex [in]

Specifies which stream to query. The value can be any of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0–0xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
The zero-based index of a stream.  To get the number of streams, call <a href="https://msdn.microsoft.com/0CD466EF-4753-42F6-A9B9-71CBB0668342">IMFCaptureSource::GetDeviceStreamCount</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM"></a><a id="mf_capture_engine_first_source_photo_stream"></a><dl>
<dt><b><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM</b></b></dt>
<dt>0xFFFFFFFB</dt>
</dl>
</td>
<td width="60%">
The first image stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM"></a><a id="mf_capture_engine_first_source_video_stream"></a><dl>
<dt><b><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM</b></b></dt>
<dt>0xFFFFFFFC</dt>
</dl>
</td>
<td width="60%">
The first video stream.

</td>
</tr>
<tr>
<td width="40%"><a id="MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM"></a><a id="mf_capture_engine_first_source_audio_stream"></a><dl>
<dt><b><b>MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM</b></b></dt>
<dt>0xFFFFFFFD</dt>
</dl>
</td>
<td width="60%">
The first audio stream.

</td>
</tr>
</table>
 


### -param ppMediaType [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/f1d60bec-71e4-4fcc-a020-92754b6f3c02">IMFMediaType</a> interface. The caller must release the interface.




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
<dt><b>MF_E_INVALIDSTREAMNUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwSourceStreamIndex</i> parameter is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

