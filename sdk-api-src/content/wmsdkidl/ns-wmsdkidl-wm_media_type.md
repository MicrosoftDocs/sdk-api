---
UID: NS:wmsdkidl._WMMediaType
title: WM_MEDIA_TYPE (wmsdkidl.h)
description: The WM_MEDIA_TYPE structure is the primary structure used to describe media formats for the objects of the Windows Media Format SDK. For more information about media formats and what they are used for, see Formats.
helpviewer_keywords: ["WM_MEDIA_TYPE","WM_MEDIA_TYPE structure [windows Media Format]","wmformat.wm_media_type","wmsdkidl/WM_MEDIA_TYPE"]
old-location: wmformat\wm_media_type.htm
tech.root: wmformat
ms.assetid: 37a9ac59-e152-47e1-96ee-b816cd645936
ms.date: 4/26/2023
ms.keywords: WM_MEDIA_TYPE, WM_MEDIA_TYPE structure [windows Media Format], wmformat.wm_media_type, wmsdkidl/WM_MEDIA_TYPE
req.header: wmsdkidl.h
req.include-header: Wmsdk.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only],Windows Media Format 7 SDK, or later versions of the SDK
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: WM_MEDIA_TYPE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WMMediaType
 - wmsdkidl/_WMMediaType
 - WM_MEDIA_TYPE
 - wmsdkidl/WM_MEDIA_TYPE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wmsdkidl.h
api_name:
 - WM_MEDIA_TYPE
---

# WM_MEDIA_TYPE structure


## -description

\[The feature associated with this page, [Windows Media Format 11 SDK](/windows/win32/wmformat/windows-media-format-11-sdk), is a legacy feature. It has been superseded by [Source Reader](/windows/win32/medfound/source-reader) and [Sink Writer](/windows/win32/medfound/sink-writer). **Source Reader** and **Sink Writer** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **Source Reader** and **Sink Writer** instead of **Windows Media Format 11 SDK**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>WM_MEDIA_TYPE</b> structure is the primary structure used to describe media formats for the objects of the Windows Media Format SDK. For more information about media formats and what they are used for, see <a href="/windows/desktop/wmformat/formats">Formats</a>.

## -struct-fields

### -field majortype

Major type of the media sample. For example, WMMEDIATYPE_Video specifies a video stream. For a list of possible major media types, see <a href="/windows/desktop/wmformat/media-types">Media Types</a>.

### -field subtype

Subtype of the media sample. The subtype defines a specific format (usually an encoding scheme) within a major media type. For example, WMMEDIASUBTYPE_WMV3 specifies a video stream encoded with the Windows Media Video 9 codec. Subtypes can be uncompressed or compressed. For lists of possible media subtypes, see <a href="/windows/desktop/wmformat/uncompressed-media-subtypes">Uncompressed Media Subtypes</a> and <a href="/windows/desktop/wmformat/compressed-media-subtypes">Compressed Media Subtypes</a>.

### -field bFixedSizeSamples

Set to true if the samples are of a fixed size. Compressed audio samples are of a fixed size while video samples are not.

### -field bTemporalCompression

Set to true if the samples are temporally compressed. Temporal compression is compression where some samples describe the changes in content from the previous sample, instead of describing the sample in its entirety. Only compressed video can be temporally compressed. By definition, no media type can use both fixed sized samples and temporal compression.

### -field lSampleSize

Long integer containing the size of the sample, in bytes. This member is used only if <b>bFixedSizeSamples</b> is true.

### -field formattype

GUID of the format type. The format type specifies the additional structure used to identify the media format. This structure is pointed to by <b>pbFormat</b>.

### -field pUnk

Not used. Should be <b>NULL</b>.

### -field cbFormat

Size, in bytes, of the structure pointed to by pbFormat.

### -field pbFormat

Pointer to the format structure of the media type. The structure referenced is determined by the format type <b>GUID</b>. Format types include:<table>
<tr>
<th>Media Type</th>
<th>Structure</th>
</tr>
<tr>
<td>WMFORMAT_VideoInfo</td>
<td>
<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmvideoinfoheader">WMVIDEOINFOHEADER</a>
</td>
</tr>
<tr>
<td>WMFORMAT_WaveFormatEx</td>
<td>
<a href="/previous-versions/windows/desktop/legacy/dd757720(v=vs.85)">WAVEFORMATEX</a>
</td>
</tr>
<tr>
<td>WMFORMAT_MPEG2Video</td>
<td>
<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmmpeg2videoinfo">WMMPEG2VIDEOINFO</a>
</td>
</tr>
<tr>
<td>WMFORMAT_WebStream</td>
<td>
<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmt_webstream_format">WMT_WEBSTREAM_FORMAT</a>
</td>
</tr>
<tr>
<td>WMFORMAT_Script</td>
<td>
<a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wmscriptformat">WMSCRIPTFORMAT</a>
</td>
</tr>
</table>

## -remarks

This is the same as the DirectShow structure <b>AM_MEDIA_TYPE</b> but is redefined in this SDK to avoid conflict with DirectShow names.

## -see-also

<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmediaprops-getmediatype">IWMMediaProps::GetMediaType</a>



<a href="/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmmediaprops-setmediatype">IWMMediaProps::SetMediaType</a>



<a href="/windows/desktop/wmformat/media-type-identifiers">Media Type Identifiers</a>



<a href="/windows/desktop/wmformat/media-types">Media Types</a>



<a href="/windows/desktop/wmformat/structures">Structures</a>
