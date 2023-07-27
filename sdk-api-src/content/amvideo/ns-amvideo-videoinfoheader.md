---
UID: NS:amvideo.tagVIDEOINFOHEADER
title: VIDEOINFOHEADER (amvideo.h)
description: The VIDEOINFOHEADER structure describes the bitmap and color information for a video image.
helpviewer_keywords: ["VIDEOINFOHEADER","VIDEOINFOHEADER structure [DirectShow]","VIDEOINFOHEADERStructure","amvideo/VIDEOINFOHEADER","dshow.videoinfoheader","tagVIDEOINFOHEADER"]
old-location: dshow\videoinfoheader.htm
tech.root: dshow
ms.assetid: a175592b-0dc1-4001-b52f-785407965932
ms.date: 4/26/2023
ms.keywords: VIDEOINFOHEADER, VIDEOINFOHEADER structure [DirectShow], VIDEOINFOHEADERStructure, amvideo/VIDEOINFOHEADER, dshow.videoinfoheader, tagVIDEOINFOHEADER
req.header: amvideo.h
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
req.typenames: VIDEOINFOHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVIDEOINFOHEADER
 - amvideo/tagVIDEOINFOHEADER
 - VIDEOINFOHEADER
 - amvideo/VIDEOINFOHEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - amvideo.h
api_name:
 - VIDEOINFOHEADER
---

# VIDEOINFOHEADER structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VIDEOINFOHEADER</b> structure describes the bitmap and color information for a video image.

## -struct-fields

### -field rcSource

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the source video window. This structure can be a clipping rectangle, to select a portion of the source video stream.

### -field rcTarget

A <a href="/windows/desktop/api/windef/ns-windef-rect">RECT</a> structure that specifies the destination video window.

### -field dwBitRate

Approximate data rate of the video stream, in bits per second.

### -field dwBitErrorRate

Data error rate, in bit errors per second.

### -field AvgTimePerFrame

The desired average display time of the video frames, in 100-nanosecond units. The actual time per frame may be longer. See Remarks.

### -field bmiHeader

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that contains color and dimension information for the video image bitmap. If the format block contains a color table or color masks, they immediately follow the <b>bmiHeader</b> member. You can get the first color entry by casting the address of member to a <b>BITMAPINFO</b> pointer.

When used inside a <b>VIDEOINFOHEADER</b> structure, the semantics of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure differ slightly from how the structure is used in GDI. For more information, refer to the topic <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER Structure</a>.

## -remarks

For information about using the <b>rcSource</b> and <b>rcTarget</b> members, see <a href="/windows/desktop/DirectShow/source-and-target-rectangles-in-video-renderers">Source and Target Rectangles in Video Renderers</a>.

<h3><a id="Frame_Rates"></a><a id="frame_rates"></a><a id="FRAME_RATES"></a>Frame Rates</h3>
The value of <b>AvgTimePerFrame</b> is usually set by the source filter, which obtains the value from the media stream. This value can be used to calculate the authored frame rate, which is the intended frame rate for the video to be rendered. During playback, the system may not be able to render the stream at the authored rate, so the actual frame rate may be less. This can happen if the machine's resources become over-committed. Also, the monitor's refresh rate can interfere with the playback rate of the video. For example, if the intended rate is 60,000/1001 (NTSC TV) and the monitor's refresh rate is 60Hz, the intended rate and the actual rate will never match. To retrieve the actual frame rate achieved during playback, use the <a href="/previous-versions/ms786607(v=vs.85)">IQualProp::get_AvgFrameRate</a> method on the video renderer.

During playback, applications can retrieve the authored frame rate as follows: 

<ul>
<li>If the old <a href="/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter is rendering, call the <a href="/windows/desktop/api/control/nf-control-ibasicvideo-get_avgtimeperframe">IBasicVideo::get_AvgTimePerFrame</a> method.</li>
<li>If the Video Mixing Renderer (VMR) is rendering, call <a href="/windows/desktop/api/strmif/nf-strmif-ipin-connectionmediatype">IPin::ConnectionMediaType</a> on the input pin and examine the format block. The VMR supports multiple input streams, and they are not required to have the same frame rates.</li>
</ul>

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>