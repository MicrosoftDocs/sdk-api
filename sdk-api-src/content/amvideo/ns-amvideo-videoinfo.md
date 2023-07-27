---
UID: NS:amvideo.tagVIDEOINFO
title: VIDEOINFO (amvideo.h)
description: The VIDEOINFO structure is equivalent to a VIDEOINFOHEADER structure, but it contains enough memory to hold three color masks plus a color table with 256 colors.If you are writing a video filter, you can use this structure to guarantee that the format block always has enough memory to contain the largest possible VIDEOINFOHEADER structure.
helpviewer_keywords: ["VIDEOINFO","VIDEOINFO structure [DirectShow]","VIDEOINFOStructure","amvideo/VIDEOINFO","dshow.videoinfo"]
old-location: dshow\videoinfo.htm
tech.root: dshow
ms.assetid: f08a449c-fed4-400b-a2fc-817bd59ba3fd
ms.date: 4/26/2023
ms.keywords: VIDEOINFO, VIDEOINFO structure [DirectShow], VIDEOINFOStructure, amvideo/VIDEOINFO, dshow.videoinfo
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
req.typenames: VIDEOINFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagVIDEOINFO
 - amvideo/tagVIDEOINFO
 - VIDEOINFO
 - amvideo/VIDEOINFO
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
 - VIDEOINFO
---

# VIDEOINFO structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>VIDEOINFO</b> structure is equivalent to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure, but it contains enough memory to hold three color masks plus a color table with 256 colors.

If you are writing a video filter, you can use this structure to guarantee that the format block always has enough memory to contain the largest possible <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

## -struct-fields

### -field rcSource

Portion of the input video to use.

### -field rcTarget

Where the video should be displayed.

### -field dwBitRate

Approximate data rate in bits per second.

### -field dwBitErrorRate

Bit error rate for this stream.

### -field AvgTimePerFrame

The desired average time per frame, in 100-nanosecond units. For more information, see the Remarks section for the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure.

### -field bmiHeader

<a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure that contains color and dimension information for a device-independent bitmap.

### -field bmiColors

Array of Win32 <a href="/windows/desktop/api/wingdi/ns-wingdi-rgbquad">RGBQUAD</a> structures that specifies the video's color palette. Each structure represents a single color, which is a combination of red, green, and blue intensities.

### -field dwBitMasks

Array of <b>DWORD</b> values that specify true-color bitmasks.

### -field TrueColorInfo

<a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-truecolorinfo">TRUECOLORINFO</a> structure that contains both a color palette and an array of color bitmasks.

## -remarks

Never use this structure unless you are sure that you will use it only to store standard RGB formats. If you store anything other than standard RGB, the variable size of the <b>bmiHeader</b> structure will almost certainly cause problems, and you should use the <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure instead. If you find it absolutely necessary to use the <b>VIDEOINFO</b> structure, do not access the <b>TrueColorInfo</b>, <b>dwBitMasks</b>, or <b>bmiColors</b> members directly. Instead, use the <a href="/previous-versions/windows/desktop/legacy/dd407230(v=vs.85)">TRUECOLOR</a>, <a href="/windows/desktop/api/amvideo/nf-amvideo-colors">COLORS</a>, and <a href="/windows/desktop/api/amvideo/nf-amvideo-bitmasks">BITMASKS</a> macros to return the pointers to the color information. Which of these members is valid depends on the contents of the <a href="/windows/desktop/api/wingdi/ns-wingdi-bitmapinfoheader">BITMAPINFOHEADER</a> structure.

The first five data members are equivalent to a <a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader">VIDEOINFOHEADER</a> structure. They are expanded in full simply to reduce the amount of dereferencing needed when dealing with a pointer to a <b>VIDEOINFO</b> structure.

For information about using the <b>rcSource</b> and <b>rcTarget</b> members, see <a href="/windows/desktop/DirectShow/source-and-target-rectangles-in-video-renderers">Source and Target Rectangles in Video Renderers</a>.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>