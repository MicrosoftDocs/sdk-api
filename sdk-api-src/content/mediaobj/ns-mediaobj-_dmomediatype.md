---
UID: NS:mediaobj._DMOMediaType
title: "_DMOMediaType"
author: windows-sdk-content
description: The DMO_MEDIA_TYPE structure describes the format of the data used by a stream in a Microsoft DirectX Media Object (DMO).
old-location: dshow\dmo_media_type.htm
tech.root: DirectShow
ms.assetid: c545ddf7-9797-45ab-a42a-d8550b598e98
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DMO_MEDIA_TYPE, DMO_MEDIA_TYPE structure [DirectShow], DMO_MEDIA_TYPEStructure, FORMAT_DvInfo, FORMAT_MPEG2Video, FORMAT_MPEGVideo, FORMAT_None, FORMAT_VideoInfo, FORMAT_VideoInfo2, FORMAT_WaveFormatEx, _DMOMediaType, dshow.dmo_media_type, mediaobj/DMO_MEDIA_TYPE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mediaobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - HeaderDef
api_location:
 - Mediaobj.h
api_name:
 - DMO_MEDIA_TYPE
product: Windows
targetos: Windows
req.typenames: DMO_MEDIA_TYPE
req.redist: 
---

# _DMOMediaType structure


## -description



The <b>DMO_MEDIA_TYPE</b> structure describes the format of the data used by a stream in a Microsoft DirectX Media Object (DMO).




## -struct-fields




### -field majortype

Major type GUID of the stream.


### -field subtype

Subtype GUID of the stream.


### -field bFixedSizeSamples

If <b>TRUE</b>, samples are of a fixed size. This field is informational only. For audio, it is generally set to <b>TRUE</b>. For video, it is usually <b>TRUE</b> for uncompressed video and <b>FALSE</b> for compressed video.


### -field bTemporalCompression

If <b>TRUE</b>, samples are compressed using temporal (interframe) compression. (A value of <b>TRUE</b> indicates that not all frames are key frames.) This field is informational only.


### -field lSampleSize

Size of the sample in bytes. For compressed data, the value can be zero.


### -field formattype

GUID specifying the format type. The <b>pbFormat</b> member points to the corresponding format structure. Format types include the following.

<table>
<tr>
<th>Format type</th>
<th>Format structure</th>
</tr>
<tr>
<td width="40%"><a id="FORMAT_DvInfo"></a><a id="format_dvinfo"></a><a id="FORMAT_DVINFO"></a><dl>
<dt><b>FORMAT_DvInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/285a56fc-9c25-4c5a-ae6a-146c17b00e84">DVINFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MPEG2Video"></a><a id="format_mpeg2video"></a><a id="FORMAT_MPEG2VIDEO"></a><dl>
<dt><b>FORMAT_MPEG2Video</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1a6ab686-99a1-40c2-addf-7fa215e2311a">MPEG2VIDEOINFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MPEGVideo"></a><a id="format_mpegvideo"></a><a id="FORMAT_MPEGVIDEO"></a><dl>
<dt><b>FORMAT_MPEGVideo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/ae5b8825-7c1c-4a44-b665-098732e6c3bc">MPEG1VIDEOINFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_None"></a><a id="format_none"></a><a id="FORMAT_NONE"></a><dl>
<dt><b>FORMAT_None</b></dt>
</dl>
</td>
<td width="60%">
None.

</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_VideoInfo"></a><a id="format_videoinfo"></a><a id="FORMAT_VIDEOINFO"></a><dl>
<dt><b>FORMAT_VideoInfo</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/a175592b-0dc1-4001-b52f-785407965932">VIDEOINFOHEADER</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_VideoInfo2"></a><a id="format_videoinfo2"></a><a id="FORMAT_VIDEOINFO2"></a><dl>
<dt><b>FORMAT_VideoInfo2</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/5e3d5bf0-435f-45da-8409-a1463b56a7ae">VIDEOINFOHEADER2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_WaveFormatEx"></a><a id="format_waveformatex"></a><a id="FORMAT_WAVEFORMATEX"></a><dl>
<dt><b>FORMAT_WaveFormatEx</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/4f3bf6fb-b15f-43b3-82f1-e7a8a3007057">WAVEFORMATEX</a>


</td>
</tr>
</table>
 


### -field pUnk

Not used. Set to <b>NULL</b>.


### -field cbFormat

Size of the format block of the media type.


### -field pbFormat

Pointer to the format structure. The structure type is specified by the <b>formattype</b> member. The format structure must be present, unless <b>formattype</b> is GUID_NULL or FORMAT_None.


## -remarks



This structure is identical to the DirectShow <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure. The <b>bFixedSizeSamples</b>, <b>bTemporalCompression</b>, and <b>lSampleSize</b> members are for compatibility with DirectShow. Other DMO clients are not required to use them.




## -see-also




<a href="https://msdn.microsoft.com/82c8ea74-1c5e-4370-9075-6db2ed6b2c91">DMO Structures</a>
 

 

