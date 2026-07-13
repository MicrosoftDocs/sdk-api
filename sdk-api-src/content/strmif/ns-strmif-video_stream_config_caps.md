---
UID: NS:strmif._VIDEO_STREAM_CONFIG_CAPS
title: VIDEO_STREAM_CONFIG_CAPS (strmif.h)
description: The VIDEO_STREAM_CONFIG_CAPS structure describes a range of video formats. Video compression and video capture filters use this structure to describe what formats they can produce.
helpviewer_keywords: ["0","1","2","3 and higher","VIDEO_STREAM_CONFIG_CAPS","VIDEO_STREAM_CONFIG_CAPS structure [DirectShow]","VIDEO_STREAM_CONFIG_CAPSStructure","dshow.video_stream_config_caps","strmif/VIDEO_STREAM_CONFIG_CAPS"]
old-location: dshow\video_stream_config_caps.htm
tech.root: dshow
ms.assetid: c4e68065-79d0-4e2e-abe5-2e5b6a51bd40
ms.date: 4/26/2023
ms.keywords: 0, 1, 2, 3 and higher, VIDEO_STREAM_CONFIG_CAPS, VIDEO_STREAM_CONFIG_CAPS structure [DirectShow], VIDEO_STREAM_CONFIG_CAPSStructure, dshow.video_stream_config_caps, strmif/VIDEO_STREAM_CONFIG_CAPS
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
req.typenames: VIDEO_STREAM_CONFIG_CAPS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _VIDEO_STREAM_CONFIG_CAPS
 - strmif/_VIDEO_STREAM_CONFIG_CAPS
 - VIDEO_STREAM_CONFIG_CAPS
 - strmif/VIDEO_STREAM_CONFIG_CAPS
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
 - VIDEO_STREAM_CONFIG_CAPS
---

# VIDEO_STREAM_CONFIG_CAPS structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VIDEO_STREAM_CONFIG_CAPS</b> structure describes a range of video formats. Video compression and video capture filters use this structure to describe what formats they can produce.
        
<div class="alert"><b>Note</b>   Most of this  structure is deprecated, with the exception of the following structure members:<ul>
<li><b>guid</b></li>
<li><b>VideoStandard</b></li>
<li><b>MinFrameInterval</b></li>
<li><b>MaxFrameInterval</b></li>
</ul> Applications can use <b>MinFrameInterval</b> and <b>MaxFrameInterval</b> to get the range of supported frame rates  from a video capture device. Applications should avoid using any of the other members of this structure. Instead, use the   <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure returned by the <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getformat">IAMStreamConfig::GetFormat</a> method.</div><div> </div>

## -struct-fields

### -field guid

<b>GUID</b> that identifies the format type. For example, <b>FORMAT_VideoInfo</b> or <b>FORMAT_VideoInfo2</b>. For more information, see the <b>formattype</b> member of the <a href="/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a> structure.

### -field VideoStandard

The analog video standard supported. The value is a bitwise combination of flags from the [AnalogVideoStandard](/windows/desktop/api/strmif/ne-strmif-analogvideostandard) enumeration type, or zero.

### -field InputSize

Native size of the incoming video signal. For a compressor, the size is taken from the input pin. For a capture filter, the size is the largest signal the filter can digitize with every pixel remaining unique.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MinCroppingSize

Smallest source rectangle allowed. The source rectangle is defined in the <b>rcSource</b> member of the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> or <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a> structure.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MaxCroppingSize

Largest source rectangle allowed.

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field CropGranularityX

Horizontal granularity of the source rectangle. This value specifies the increments that are valid between <b>MinCroppingSize</b> and <b>MaxCroppingSize</b>.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field CropGranularityY

Vertical granularity of the source rectangle. This value specifies the increments that are valid between <b>MinCroppingSize</b> and <b>MaxCroppingSize</b>.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field CropAlignX

Required horizontal alignment of the source rectangle.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field CropAlignY

Required vertical alignment of the source rectangle.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MinOutputSize

Minimum output size.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MaxOutputSize

Maximum output size.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field OutputGranularityX

Granularity of the output width. This value specifies the increments that are valid between <b>MinOutputSize</b> and <b>MaxOutputSize</b>.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field OutputGranularityY

Granularity of output height. This value specifies the increments that are valid between <b>MinOutputSize</b> and <b>MaxOutputSize</b>.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field StretchTapsX

Indicates how well the filter can stretch the image horizontally.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field StretchTapsY

Indicates how well the filter can stretch the image vertically.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field ShrinkTapsX

Indicates how well the filter can shrink the image horizontally.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field ShrinkTapsY

Indicates how well the filter can shrink the image vertically.

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>
The previous four structure members use the following values:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
Does not support stretching/shrinking. 

</td>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Uses pixel doubling (stretching) or eliminates pixels (shrinking) 

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Uses interpolation (2 taps) 

</td>
</tr>
<tr>
<td width="40%"><a id="3_and_higher"></a><a id="3_AND_HIGHER"></a><dl>
<dt><b>3 and higher</b></dt>
</dl>
</td>
<td width="60%">
Uses interpolation (&gt;2 taps) 

</td>
</tr>
</table>

### -field MinFrameInterval

The minimum frame duration, in 100-nanosecond units. This value applies only to capture filters.

### -field MaxFrameInterval

The maximum frame duration, in 100-nanosecond units. This value applies only to capture filters.

### -field MinBitsPerSecond

Minimum data rate this pin can produce.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

### -field MaxBitsPerSecond

Maximum data rate this pin can produce.
          

<div class="alert"><b>Note</b>  Deprecated.</div>
<div> </div>

## -remarks

The <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getstreamcaps">IAMStreamConfig::GetStreamCaps</a> method returns this structure. An application can use this information to modify the output format on a video compression filter or video capture filter.
      

For example, assume that filter returns the following values for the source rectangle:
        

<ul>
<li>MinCroppingSize = (160, 120)</li>
<li>MaxCroppingSize = (320, 240)</li>
<li>CropGranularityX = 4</li>
<li>CropGranularityY = 8</li>
<li>CropAlignX = 2</li>
<li>CropAlignY = 4</li>
</ul>
These numbers define the set of rectangles that are valid for the <b>rcSource</b> member of the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> or <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a> structure. In this example, the minimum source rectangle is 160 pixels wide x 120 pixels high. The width can be increased in steps of 4 pixels, to a maximum of 320. The height can be increased in steps of 8 pixels, to a maximum of 240. In other words, the valid widths are 160, 164, 168 ... 320; and the valid heights are 120, 128, 136 ... 240.

The <b>CropAlignX</b> and <b>CropAlignY</b> members define where the top-left corner of the source rectangle can sit. For example, the following rectangles are valid, given the previous values:

<ul>
<li>(0, 0, 160, 120)</li>
<li>(2, 0, 162, 120)</li>
<li>(2, 8, 162, 128)</li>
</ul>
In a similar way, the <b>MinOutputSize</b>, <b>MaxOutputSize</b>, <b>OutputGranularityX</b>, and <b>OutputGranularityY</b> members define what values are supported for the <b>biWidth</b> and <b>biHeight</b> members of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

For capture filters, the <b>MinFrameInterval</b> and <b>MaxFrameInterval</b> members define the minimum and maximum duration of each frame, as given in the <b>AvgTimePerFrame</b> member of the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> or <a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2">VIDEOINFOHEADER2</a> structure. The filter may not support every frame rate that falls between these two values. The <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-setformat">IAMStreamConfig::SetFormat</a> method will set the frame rate to the closest value that the filter supports. If <b>SetFormat</b> succeeds, call <a href="/windows/desktop/api/strmif/nf-strmif-iamstreamconfig-getformat">IAMStreamConfig::GetFormat</a> to determine the actual frame rate.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>