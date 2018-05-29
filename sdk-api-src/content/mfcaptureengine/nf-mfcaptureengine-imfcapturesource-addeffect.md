---
UID: NF:mfcaptureengine.IMFCaptureSource.AddEffect
title: IMFCaptureSource::AddEffect
author: windows-sdk-content
description: Adds an effect to a capture stream.
old-location: mf\imfcapturesource_addeffect.htm
old-project: medfound
ms.assetid: C108360D-0B8C-4539-9D78-A5559100086E
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: AddEffect, AddEffect method [Media Foundation], AddEffect method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],AddEffect method, IMFCaptureSource.AddEffect, IMFCaptureSource::AddEffect, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, mf.imfcapturesource_addeffect, mfcaptureengine/IMFCaptureSource::AddEffect
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
req.typenames: MF_CAPTURE_ENGINE_STREAM_CATEGORY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfcaptureengine.h
api_name:
-	IMFCaptureSource.AddEffect
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFCaptureSource::AddEffect


## -description


Adds an effect to a capture stream.


## -parameters




### -param dwSourceStreamIndex [in]

The capture stream. The value can be any of the following.

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
 


### -param pUnknown [in]

A pointer to one of the following:



<ul>
<li>A Media Foundation transform (MFT) that exposes the <a href="https://msdn.microsoft.com/3cc502d8-d364-43b9-b0b6-d9474c002b20">IMFTransform</a> interface.</li>
<li>An MFT activation object that exposes the <a href="https://msdn.microsoft.com/c0936e3c-3cd1-4c1e-a336-2dee7d943963">IMFActivate</a> interface.</li>
</ul>

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
<dt><b>MF_E_INVALIDMEDIATYPE</b></dt>
</dl>
</td>
<td width="60%">
No compatible media type could be found.

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
 




## -remarks



The effect must be implemented as a <a href="https://msdn.microsoft.com/cb23fe0a-c42c-4912-a0bf-1f0b18a6f4e0">Media Foundation Transform</a> (MFT). The <i>pUnknown</i> parameter can point to an instance of the MFT, or to an activation object for the MFT. For more information, see <a href="https://msdn.microsoft.com/767d5f1c-2b8d-43b6-916b-035129e93204">Activation Objects</a>.

The effect is applied to the stream before the data reaches the capture sinks. 




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

