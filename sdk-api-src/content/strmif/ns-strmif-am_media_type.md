---
UID: NS:strmif._AMMediaType
title: AM_MEDIA_TYPE (strmif.h)
description: The AM_MEDIA_TYPE structure describes the format of a media sample.
helpviewer_keywords: ["AM_MEDIA_TYPE","AM_MEDIA_TYPE structure [DirectShow]","AM_MEDIA_TYPEStructure","FORMAT_DvInfo","FORMAT_MPEG2Video","FORMAT_MPEGStreams","FORMAT_MPEGVideo","FORMAT_None","FORMAT_VideoInfo","FORMAT_VideoInfo2","FORMAT_WaveFormatEx","GUID_NULL","_AMMediaType","dshow.am_media_type","strmif/AM_MEDIA_TYPE"]
old-location: dshow\am_media_type.htm
tech.root: dshow
ms.assetid: 973697d0-2897-48b5-88ca-a88a9650eb02
ms.date: 4/26/2023
ms.keywords: AM_MEDIA_TYPE, AM_MEDIA_TYPE structure [DirectShow], AM_MEDIA_TYPEStructure, FORMAT_DvInfo, FORMAT_MPEG2Video, FORMAT_MPEGStreams, FORMAT_MPEGVideo, FORMAT_None, FORMAT_VideoInfo, FORMAT_VideoInfo2, FORMAT_WaveFormatEx, GUID_NULL, _AMMediaType, dshow.am_media_type, strmif/AM_MEDIA_TYPE
req.header: strmif.h
req.include-header: Dshow.h
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
targetos: Windows
req.typenames: AM_MEDIA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AMMediaType
 - strmif/_AMMediaType
 - AM_MEDIA_TYPE
 - strmif/AM_MEDIA_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - AM_MEDIA_TYPE
---

# AM_MEDIA_TYPE structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AM_MEDIA_TYPE</b> structure describes the format of a media sample.

## -struct-fields

### -field majortype

Globally unique identifier (GUID) that specifies the major type of the media sample. For a list of possible major types, see <a href="/windows/desktop/DirectShow/media-types">Media Types</a>.

### -field subtype

GUID that specifies the subtype of the media sample. For a list of possible subtypes, see <a href="/windows/desktop/DirectShow/media-types">Media Types</a>. For some formats, the value might be MEDIASUBTYPE_None, which means the format does not require a subtype.

### -field bFixedSizeSamples

If <b>TRUE</b>, samples are of a fixed size. This field is informational only. For audio, it is generally set to <b>TRUE</b>. For video, it is usually <b>TRUE</b> for uncompressed video and <b>FALSE</b> for compressed video.

### -field bTemporalCompression

If <b>TRUE</b>, samples are compressed using temporal (interframe) compression. A value of <b>TRUE</b> indicates that not all frames are key frames. This field is informational only.

### -field lSampleSize

Size of the sample in bytes. For compressed data, the value can be zero.

### -field formattype

GUID that specifies the structure used for the format block. The <b>pbFormat</b> member points to the corresponding format structure. Format types include the following:

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

<a href="/windows/desktop/api/strmif/ns-strmif-dvinfo">DVINFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MPEG2Video"></a><a id="format_mpeg2video"></a><a id="FORMAT_MPEG2VIDEO"></a><dl>
<dt><b>FORMAT_MPEG2Video</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo">MPEG2VIDEOINFO</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MPEGStreams"></a><a id="format_mpegstreams"></a><a id="FORMAT_MPEGSTREAMS"></a><dl>
<dt><b>FORMAT_MPEGStreams</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/api/mpegtype/ns-mpegtype-am_mpegsystemtype">AM_MPEGSYSTEMTYPE</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_MPEGVideo"></a><a id="format_mpegvideo"></a><a id="FORMAT_MPEGVIDEO"></a><dl>
<dt><b>FORMAT_MPEGVideo</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo">MPEG1VIDEOINFO</a>


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

<a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_VideoInfo2"></a><a id="format_videoinfo2"></a><a id="FORMAT_VIDEOINFO2"></a><dl>
<dt><b>FORMAT_VideoInfo2</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a>


</td>
</tr>
<tr>
<td width="40%"><a id="FORMAT_WaveFormatEx"></a><a id="format_waveformatex"></a><a id="FORMAT_WAVEFORMATEX"></a><dl>
<dt><b>FORMAT_WaveFormatEx</b></dt>
</dl>
</td>
<td width="60%">

<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>


</td>
</tr>
<tr>
<td width="40%"><a id="GUID_NULL"></a><a id="guid_null"></a><dl>
<dt><b>GUID_NULL</b></dt>
</dl>
</td>
<td width="60%">
None

</td>
</tr>
</table>

### -field pUnk

Not used. Set to <b>NULL</b>.

### -field cbFormat

Size of the format block, in bytes.

### -field pbFormat

Pointer to the format block. The structure type is specified by the <b>formattype</b> member. The format structure must be present, unless <b>formattype</b> is GUID_NULL or FORMAT_None.
          

The <b>pbFormat</b> buffer must be allocated by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a>. To release the format block, call <a href="/windows/desktop/DirectShow/freemediatype">FreeMediaType</a>.

## -remarks

When two pins connect, they negotiate a media type, which is defined by an <b>AM_MEDIA_TYPE</b> structure. The media type describes the format of the data that the filters will exchange. If the filters do not agree on a media type, they cannot connect.

The stream type is specified by two <b>GUID</b>s, called the <i>major type</i> and the <i>subtype</i>. The major type defines the general category, such as video, audio, or byte stream. The subtype defines a narrower category within the major type. For example, video subtypes include 8-bit, 16-bit, 24-bit, and 32-bit RGB.

The <b>AM_MEDIA_TYPE</b> structure is followed by a variable-length block of data that contains format-specific information. The <b>pbFormat</b> member points to this block, called the <i>format block</i>. The layout of the format block depends on the type of data in the stream, and is specified by the <b>formattype</b> member. The format block might be <b>NULL</b>. Check the <b>cbFormat</b> member to determine the size. Cast the <b>pbFormat</b> member to access the format block. For example:

<div class="code"><span><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
if (pmt-&gt;formattype == FORMAT_VideoInfo)
{
    // Check the buffer size.
    if (pmt-&gt;cbFormat &gt;= sizeof(VIDEOINFOHEADER))
    {
        VIDEOINFOHEADER *pVih = 
            reinterpret_cast&lt;VIDEOINFOHEADER*&gt;(pmt-&gt;pbFormat);
        /* Access VIDEOINFOHEADER members through pVih. */
    }
}
</pre>
</td>
</tr>
</table></span></div>
In some situations, you can set the format block to <b>NULL</b> and the format type to GUID_NULL, resulting in a <i>partial media type</i>. This enables you to specify a range of possible formats. For example, you can specify 24-bit RGB (MEDIASUBTYPE_RGB24) without giving an exact width or height.

To obtain detailed information about a specified media type for debugging purposes, use the <a href="/windows/desktop/DirectShow/displaytype">DisplayType</a> method.

## -see-also

<a href="/windows/desktop/DirectShow/about-media-types">About Media Types</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/media-type-functions">Media Type Functions</a>



<a href="/windows/desktop/DirectShow/media-types">Media Types</a>