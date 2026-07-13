---
UID: NS:vfw._AVISTREAMINFOW
title: AVISTREAMINFOW (vfw.h)
description: The AVISTREAMINFO structure contains information for a single stream. (Unicode)
helpviewer_keywords: ["*LPAVISTREAMINFOW","AVISTREAMINFO","AVISTREAMINFO structure [Windows Multimedia]","AVISTREAMINFOA","AVISTREAMINFOW","AVISTREAMINFO_DISABLED","AVISTREAMINFO_FORMATCHANGES","multimedia.avistreaminfo_COLLISION869","multimedia.avistreaminfo_struct","streamtypeAUDIO","streamtypeMIDI","streamtypeTEXT","streamtypeVIDEO","vfw/AVISTREAMINFO"]
old-location: multimedia\avistreaminfo_struct.htm
tech.root: Multimedia
ms.assetid: dca6d9ca-a825-4bd0-a19d-0655d775fdfb
ms.date: 12/05/2018
ms.keywords: '*LPAVISTREAMINFOW, AVISTREAMINFO, AVISTREAMINFO structure [Windows Multimedia], AVISTREAMINFOA, AVISTREAMINFOW, AVISTREAMINFO_DISABLED, AVISTREAMINFO_FORMATCHANGES, multimedia.avistreaminfo_COLLISION869, multimedia.avistreaminfo_struct, streamtypeAUDIO, streamtypeMIDI, streamtypeTEXT, streamtypeVIDEO, vfw/AVISTREAMINFO'
req.header: vfw.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AVISTREAMINFOW
 - vfw/_AVISTREAMINFOW
 - LPAVISTREAMINFOW
 - vfw/LPAVISTREAMINFOW
 - AVISTREAMINFOW
 - vfw/AVISTREAMINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVISTREAMINFO
---

# AVISTREAMINFOW structure


## -description

The <b>AVISTREAMINFO</b> structure contains information for a single stream.

## -struct-fields

### -field fccType

Four-character code indicating the stream type. The following constants have been defined for the data commonly found in AVI streams:

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="streamtypeAUDIO"></a><a id="streamtypeaudio"></a><a id="STREAMTYPEAUDIO"></a><dl>
<dt><b>streamtypeAUDIO</b></dt>
</dl>
</td>
<td width="60%">
Indicates an audio stream.

</td>
</tr>
<tr>
<td width="40%"><a id="streamtypeMIDI"></a><a id="streamtypemidi"></a><a id="STREAMTYPEMIDI"></a><dl>
<dt><b>streamtypeMIDI</b></dt>
</dl>
</td>
<td width="60%">
Indicates a MIDI stream.

</td>
</tr>
<tr>
<td width="40%"><a id="streamtypeTEXT"></a><a id="streamtypetext"></a><a id="STREAMTYPETEXT"></a><dl>
<dt><b>streamtypeTEXT</b></dt>
</dl>
</td>
<td width="60%">
Indicates a text stream.

</td>
</tr>
<tr>
<td width="40%"><a id="streamtypeVIDEO"></a><a id="streamtypevideo"></a><a id="STREAMTYPEVIDEO"></a><dl>
<dt><b>streamtypeVIDEO</b></dt>
</dl>
</td>
<td width="60%">
Indicates a video stream.

</td>
</tr>
</table>

### -field fccHandler

Four-character code of the compressor handler that will compress this video stream when it is saved (for example, <a href="/windows/desktop/api/vfw/nf-vfw-mmiofourcc">mmioFOURCC</a> ('M','S','V','C')). This member is not used for audio streams.

### -field dwFlags

Applicable flags for the stream. The bits in the high-order word of these flags are specific to the type of data contained in the stream. The following flags are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AVISTREAMINFO_DISABLED"></a><a id="avistreaminfo_disabled"></a><dl>
<dt><b>AVISTREAMINFO_DISABLED</b></dt>
</dl>
</td>
<td width="60%">
Indicates this stream should be rendered when explicitly enabled by the user.

</td>
</tr>
<tr>
<td width="40%"><a id="AVISTREAMINFO_FORMATCHANGES"></a><a id="avistreaminfo_formatchanges"></a><dl>
<dt><b>AVISTREAMINFO_FORMATCHANGES</b></dt>
</dl>
</td>
<td width="60%">
Indicates this video stream contains palette changes. This flag warns the playback software that it will need to animate the palette.

</td>
</tr>
</table>

### -field dwCaps

Capability flags; currently unused.

### -field wPriority

Priority of the stream.

### -field wLanguage

Language of the stream.

### -field dwScale

Time scale applicable for the stream. Dividing <b>dwRate</b> by <b>dwScale</b> gives the playback rate in number of samples per second.

For video streams, this rate should be the frame rate. For audio streams, this rate should correspond to the audio block size (the <b>nBlockAlign</b> member of the <a href="/windows/win32/api/mmeapi/ns-mmeapi-waveformatex">WAVEFORMAT</a> or <a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a> structure), which for PCM (Pulse Code Modulation) audio reduces to the sample rate.

### -field dwRate

Rate in an integer format. To obtain the rate in samples per second, divide this value by the value in <b>dwScale</b>.

### -field dwStart

Sample number of the first frame of the AVI file. The units are defined by dwRate and <b>dwScale</b>. Normally, this is zero, but it can specify a delay time for a stream that does not start concurrently with the file.

The 1.0 release of the AVI tools does not support a nonzero starting time.

### -field dwLength

Length of this stream. The units are defined by <b>dwRate</b> and <b>dwScale</b>.

### -field dwInitialFrames

Audio skew. This member specifies how much to skew the audio data ahead of the video frames in interleaved files. Typically, this is about 0.75 seconds.

### -field dwSuggestedBufferSize

Recommended buffer size, in bytes, for the stream. Typically, this member contains a value corresponding to the largest chunk in the stream. Using the correct buffer size makes playback more efficient. Use zero if you do not know the correct buffer size.

### -field dwQuality

Quality indicator of the video data in the stream. Quality is represented as a number between 0 and 10,000. For compressed data, this typically represents the value of the quality parameter passed to the compression software. If set to –1, drivers use the default quality value.

### -field dwSampleSize

Size, in bytes, of a single data sample. If the value of this member is zero, the samples can vary in size and each data sample (such as a video frame) must be in a separate chunk. A nonzero value indicates that multiple samples of data can be grouped into a single chunk within the file.

For video streams, this number is typically zero, although it can be nonzero if all video frames are the same size. For audio streams, this number should be the same as the <b>nBlockAlign</b> member of the <a href="/windows/win32/api/mmeapi/ns-mmeapi-waveformatex">WAVEFORMAT</a> or <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure describing the audio.

### -field rcFrame

Dimensions of the video destination rectangle. The values represent the coordinates of upper left corner, the height, and the width of the rectangle.

### -field dwEditCount

Number of times the stream has been edited. The stream handler maintains this count.

### -field dwFormatChangeCount

Number of times the stream format has changed. The stream handler maintains this count.

### -field szName

Null-terminated string containing a description of the stream.

## -see-also

<a href="/windows/desktop/Multimedia/avifile-functions-and-macros">AVIFile Functions and Macros</a>



<a href="/windows/desktop/Multimedia/avifile-structures">AVIFile Structures</a>



<a href="/previous-versions/dd743663(v=vs.85)">PCMWAVEFORMAT</a>



<a href="/windows/win32/api/mmeapi/ns-mmeapi-waveformatex">WAVEFORMAT</a>



<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a>



<a href="/windows/desktop/api/vfw/nf-vfw-mmiofourcc">mmioFOURCC</a>

## -remarks

> [!NOTE]
> The vfw.h header defines AVISTREAMINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
