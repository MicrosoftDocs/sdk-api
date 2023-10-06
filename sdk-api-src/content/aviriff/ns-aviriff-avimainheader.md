---
UID: NS:aviriff._avimainheader
title: AVIMAINHEADER (aviriff.h)
description: The AVIMAINHEADER structure defines global information in an AVI file.
helpviewer_keywords: ["AVIF_COPYRIGHTED","AVIF_HASINDEX","AVIF_ISINTERLEAVED","AVIF_MUSTUSEINDEX","AVIF_WASCAPTUREFILE","AVIMAINHEADER","AVIMAINHEADER structure [DirectShow]","AVIMAINHEADERStructure","aviriff/AVIMAINHEADER","dshow.avimainheader"]
old-location: dshow\avimainheader.htm
tech.root: dshow
ms.assetid: 3b8a326c-ebb2-4fb7-a167-7382d2e78ec2
ms.date: 4/26/2023
ms.keywords: AVIF_COPYRIGHTED, AVIF_HASINDEX, AVIF_ISINTERLEAVED, AVIF_MUSTUSEINDEX, AVIF_WASCAPTUREFILE, AVIMAINHEADER, AVIMAINHEADER structure [DirectShow], AVIMAINHEADERStructure, aviriff/AVIMAINHEADER, dshow.avimainheader
req.header: aviriff.h
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
targetos: Windows
req.typenames: AVIMAINHEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _avimainheader
 - aviriff/_avimainheader
 - AVIMAINHEADER
 - aviriff/AVIMAINHEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Aviriff.h
api_name:
 - AVIMAINHEADER
---

# AVIMAINHEADER structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>AVIMAINHEADER</b> structure defines global information in an AVI file.

## -struct-fields

### -field fcc

Specifies a FOURCC code. The value must be 'avih'.

### -field cb

Specifies the size of the structure, not including the initial 8 bytes.

### -field dwMicroSecPerFrame

Specifies the number of microseconds between frames. This value indicates the overall timing for the file.

### -field dwMaxBytesPerSec

Specifies the approximate maximum data rate of the file. This value indicates the number of bytes per second the system must handle to present an AVI sequence as specified by the other parameters contained in the main header and stream header chunks.

### -field dwPaddingGranularity

Specifies the alignment for data, in bytes. Pad the data to multiples of this value.

### -field dwFlags

Contains a bitwise combination of zero or more of the following flags:
          

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="AVIF_COPYRIGHTED"></a><a id="avif_copyrighted"></a><dl>
<dt><b>AVIF_COPYRIGHTED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the AVI file contains copyrighted data and software. When this flag is used, software should not permit the data to be duplicated.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIF_HASINDEX"></a><a id="avif_hasindex"></a><dl>
<dt><b>AVIF_HASINDEX</b></dt>
</dl>
</td>
<td width="60%">
Indicates the AVI file has an index.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIF_ISINTERLEAVED"></a><a id="avif_isinterleaved"></a><dl>
<dt><b>AVIF_ISINTERLEAVED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the AVI file is interleaved.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIF_MUSTUSEINDEX"></a><a id="avif_mustuseindex"></a><dl>
<dt><b>AVIF_MUSTUSEINDEX</b></dt>
</dl>
</td>
<td width="60%">
Indicates that application should use the index, rather than the physical ordering of the chunks in the file, to determine the order of presentation of the data. For example, this flag could be used to create a list of frames for editing.

</td>
</tr>
<tr>
<td width="40%"><a id="AVIF_WASCAPTUREFILE"></a><a id="avif_wascapturefile"></a><dl>
<dt><b>AVIF_WASCAPTUREFILE</b></dt>
</dl>
</td>
<td width="60%">
Indicates the AVI file is a specially allocated file used for capturing real-time video. Applications should warn the user before writing over a file with this flag set because the user probably defragmented this file.

</td>
</tr>
</table>

### -field dwTotalFrames

Specifies the total number of frames of data in the file.

### -field dwInitialFrames

Specifies the initial frame for interleaved files. Noninterleaved files should specify zero. If you are creating interleaved files, specify the number of frames in the file prior to the initial frame of the AVI sequence in this member.

To give the audio driver enough audio to work with, the audio data in an interleaved file must be skewed from the video data. Typically, the audio data should be moved forward enough frames to allow approximately 0.75 seconds of audio data to be preloaded. The <b>dwInitialRecords</b> member should be set to the number of frames the audio is skewed. Also set the same value for the <b>dwInitialFrames</b> member of the <a href="/previous-versions/windows/desktop/api/avifmt/ns-avifmt-avistreamheader">AVISTREAMHEADER</a> structure in the audio stream header.

### -field dwStreams

Specifies the number of streams in the file. For example, a file with audio and video has two streams.

### -field dwSuggestedBufferSize

Specifies the suggested buffer size for reading the file. Generally, this size should be large enough to contain the largest chunk in the file. If set to zero, or if it is too small, the playback software will have to reallocate memory during playback, which will reduce performance. For an interleaved file, the buffer size should be large enough to read an entire record, and not just a chunk.

### -field dwWidth

Specifies the width of the AVI file in pixels.

### -field dwHeight

Specifies the height of the AVI file in pixels.

### -field dwReserved

Reserved. Set this array to zero.

## -remarks

The header file Vfw.h defines a <b>MainAVIHeader</b> structure that is equivalent to this structure, but omits the <b>fcc</b> and <b>cb</b> members.

## -see-also

<a href="/windows/desktop/DirectShow/avi-riff-file-reference">AVI RIFF File Reference</a>



<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>