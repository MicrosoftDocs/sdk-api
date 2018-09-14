---
UID: NF:mfcaptureengine.IMFCaptureSource.GetAvailableDeviceMediaType
title: IMFCaptureSource::GetAvailableDeviceMediaType
author: windows-sdk-content
description: Gets a format that is supported by one of the capture streams.
old-location: mf\imfcapturesource_getavailabledevicemediatype.htm
tech.root: medfound
ms.assetid: B122C2DE-9544-47C7-8F4F-DBD4C1DE54C0
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: GetAvailableDeviceMediaType, GetAvailableDeviceMediaType method [Media Foundation], GetAvailableDeviceMediaType method [Media Foundation],IMFCaptureSource interface, IMFCaptureSource interface [Media Foundation],GetAvailableDeviceMediaType method, IMFCaptureSource.GetAvailableDeviceMediaType, IMFCaptureSource::GetAvailableDeviceMediaType, MF_CAPTURE_ENGINE_FIRST_SOURCE_AUDIO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_PHOTO_STREAM, MF_CAPTURE_ENGINE_FIRST_SOURCE_VIDEO_STREAM, mf.imfcapturesource_getavailabledevicemediatype, mfcaptureengine/IMFCaptureSource::GetAvailableDeviceMediaType
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
 - IMFCaptureSource.GetAvailableDeviceMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureSource::GetAvailableDeviceMediaType


## -description


Gets a format that is supported by one of the capture streams.


## -parameters




### -param dwSourceStreamIndex [in]

The stream to query. The value can be any of the following.

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
The zero-based index of a stream. To get the number of streams, call <a href="https://msdn.microsoft.com/0CD466EF-4753-42F6-A9B9-71CBB0668342">IMFCaptureSource::GetDeviceStreamCount</a>.

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
 


### -param dwMediaTypeIndex [in]

The zero-based index of the media type to retrieve.


### -param ppMediaType [in]

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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_NO_MORE_TYPES</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwMediaTypeIndex</i> parameter is out of range. 


</td>
</tr>
</table>
 




## -remarks



To enumerate all of the available formats on a stream, call this method in a loop while incrementing <i>dwMediaTypeIndex</i>, until the method returns <b>MF_E_NO_MORE_TYPES</b>.

Some cameras might support a range of frame rates. The minimum and maximum frame rates are stored in the <a href="https://msdn.microsoft.com/d3725796-f683-4ca1-a37f-22c40fff0b76">MF_MT_FRAME_RATE_RANGE_MIN</a> and <a href="https://msdn.microsoft.com/8e0c4996-9f78-424e-b012-502228b6a27a">MF_MT_FRAME_RATE_RANGE_MAX</a> attributes on the media type.




## -see-also




<a href="https://msdn.microsoft.com/864B6B5D-EB7E-4C49-A326-9B6704A27635">IMFCaptureSource</a>
 

 

