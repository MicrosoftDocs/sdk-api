---
UID: NS:avifmt.AVIStreamHeader
title: AVIStreamHeader (avifmt.h)
description: The AVISTREAMHEADER structure contains information about one stream in an AVI file.
helpviewer_keywords: ["auds","mids","txts","vids","AVISF_DISABLED","AVISF_VIDEO_PALCHANGES","AVISTREAMHEADER","AVISTREAMHEADER structure [DirectShow]","AVISTREAMHEADERStructure","AVIStreamHeader","_avistreamheader","avifmt/AVISTREAMHEADER","dshow.avistreamheader"]
old-location: dshow\avistreamheader.htm
tech.root: dshow
ms.assetid: f07c28ac-2dd0-428a-a94a-32aec2bb0854
ms.date: 4/26/2023
req.header: avifmt.h
req.include-header: Aviriff.h
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
req.typenames: AVIStreamHeader
req.redist: 
ms.custom: 19H1
f1_keywords:
 - AVIStreamHeader
 - avifmt/AVIStreamHeader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - avifmt.h
api_name:
 - AVISTREAMHEADER
---

## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AVISTREAMHEADER</b> structure contains information about one stream in an AVI file.

## -struct-fields

### -field fccType

Contains a FOURCC that specifies the type of the data contained in the stream. The following standard AVI values for video and audio are defined.

<table>
<tr>
<th>FOURCC</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="_auds_"></a><a id="_AUDS_"></a><dl>
<dt><b>'auds'</b></dt>
</dl>
</td>
<td width="60%">
Audio stream

</td>
</tr>
<tr>
<td width="40%"><a id="_mids_"></a><a id="_MIDS_"></a><dl>
<dt><b>'mids'</b></dt>
</dl>
</td>
<td width="60%">
MIDI stream

</td>
</tr>
<tr>
<td width="40%"><a id="_txts_"></a><a id="_TXTS_"></a><dl>
<dt><b>'txts'</b></dt>
</dl>
</td>
<td width="60%">
Text stream

</td>
</tr>
<tr>
<td width="40%"><a id="_vids_"></a><a id="_VIDS_"></a><dl>
<dt><b>'vids'</b></dt>
</dl>
</td>
<td width="60%">
Video stream

</td>
</tr>
</table>

### -field fccHandler

Optionally, contains a FOURCC that identifies a specific data handler. The data handler is the preferred handler for the stream. For audio and video streams, this specifies the codec for decoding the stream.

### -field dwFlags

Contains any flags for the data stream. The bits in the high-order word of these flags are specific to the type of data contained in the stream. The following standard flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVISF_DISABLED"></a><a id="avisf_disabled"></a><dl>
<dt><b>AVISF_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Indicates this stream should not be enabled by default. 

</td>
</tr>
<tr>
<td width="40%"><a id="AVISF_VIDEO_PALCHANGES"></a><a id="avisf_video_palchanges"></a><dl>
<dt><b>AVISF_VIDEO_PALCHANGES</b></dt>
</dl>
</td>
<td width="60%">
Indicates this video stream contains palette changes. This flag warns the playback software that it will need to animate the palette. 

</td>
</tr>
</table>

### -field wPriority

Specifies priority of a stream type. For example, in a file with multiple audio streams, the one with the highest priority might be the default stream.

### -field wLanguage

Language tag.

### -field dwInitialFrames

Specifies how far audio data is skewed ahead of the video frames in interleaved files. Typically, this is about 0.75 seconds. If you are creating interleaved files, specify the number of frames in the file prior to the initial frame of the AVI sequence in this member. For more information, see the remarks for the <b>dwInitialFrames</b> member of the <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimainheader">AVIMAINHEADER</a> structure.

### -field dwScale

Used with <b>dwRate</b> to specify the time scale that this stream will use. Dividing <b>dwRate</b> by <b>dwScale</b> gives the number of samples per second. For video streams, this is the frame rate. For audio streams, this rate corresponds to the time needed to play <b>nBlockAlign</b> bytes of audio, which for PCM audio is the just the sample rate.

### -field dwRate

See <b>dwScale</b>.

### -field dwStart

Specifies the starting time for this stream. The units are defined by the <b>dwRate</b> and <b>dwScale</b> members in the main file header. Usually, this is zero, but it can specify a delay time for a stream that does not start concurrently with the file.

### -field dwLength

Specifies the length of this stream. The units are defined by the <b>dwRate</b> and <b>dwScale</b> members of the stream's header.

### -field dwSuggestedBufferSize

Specifies how large a buffer should be used to read this stream. Typically, this contains a value corresponding to the largest chunk present in the stream. Using the correct buffer size makes playback more efficient. Use zero if you do not know the correct buffer size.

### -field dwQuality

Specifies an indicator of the quality of the data in the stream. Quality is represented as a number between 0 and 10,000. For compressed data, this typically represents the value of the quality parameter passed to the compression software. If set to –1, drivers use the default quality value.

### -field dwSampleSize

Specifies the size of a single sample of data. This is set to zero if the samples can vary in size. If this number is nonzero, then multiple samples of data can be grouped into a single chunk within the file. If it is zero, each sample of data (such as a video frame) must be in a separate chunk. For video streams, this number is typically zero, although it can be nonzero if all video frames are the same size. For audio streams, this number should be the same as the <b>nBlockAlign</b> member of the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure describing the audio.

### -field rcFrame

Specifies the destination rectangle for a text or video stream within the movie rectangle specified by the <b>dwWidth</b> and <b>dwHeight</b> members of the AVI main header structure. The <b>rcFrame</b> member is typically used in support of multiple video streams. Set this rectangle to the coordinates corresponding to the movie rectangle to update the whole movie rectangle. Units for this member are pixels. The upper-left corner of the destination rectangle is relative to the upper-left corner of the movie rectangle.

## -remarks

Some of the members of this structure are also present in the <a href="/previous-versions/windows/desktop/api/aviriff/ns-aviriff-avimainheader">AVIMAINHEADER</a> structure. The data in the <b>AVIMAINHEADER</b> structure applies to the whole file, while the data in the <b>AVISTREAMHEADER</b> structure applies to one stream.

The header file Vfw.h defines a <b>AVIStreamHeader</b> structure that is equivalent to this structure, but omits the <b>fcc</b> and <b>cb</b> members.

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>

