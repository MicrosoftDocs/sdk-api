---
UID: NS:vfw._AVISTREAMINFOW
title: "_AVISTREAMINFOW"
author: windows-sdk-content
description: The AVISTREAMINFO structure contains information for a single stream.
old-location: multimedia\avistreaminfo_struct.htm
old-project: Multimedia
ms.assetid: dca6d9ca-a825-4bd0-a19d-0655d775fdfb
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: "*LPAVISTREAMINFOW, AVISTREAMINFO, AVISTREAMINFO structure [Windows Multimedia], AVISTREAMINFOA, AVISTREAMINFOW, AVISTREAMINFO_DISABLED, AVISTREAMINFO_FORMATCHANGES, _AVISTREAMINFOW, multimedia.avistreaminfo_COLLISION869, multimedia.avistreaminfo_struct, streamtypeAUDIO, streamtypeMIDI, streamtypeTEXT, streamtypeVIDEO, vfw/AVISTREAMINFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: AVISTREAMINFOW, *LPAVISTREAMINFOW
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVISTREAMINFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# _AVISTREAMINFOW structure


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

Four-character code of the compressor handler that will compress this video stream when it is saved (for example, <a href="https://msdn.microsoft.com/616c3b43-9305-49c1-bc46-2e1256647c7d">mmioFOURCC</a> ('M','S','V','C')). This member is not used for audio streams.


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

For video streams, this rate should be the frame rate. For audio streams, this rate should correspond to the audio block size (the <b>nBlockAlign</b> member of the <a href="https://msdn.microsoft.com/48871868-792a-4479-9e92-95306c25673a">WAVEFORMAT</a> or <a href="https://msdn.microsoft.com/c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c">PCMWAVEFORMAT</a> structure), which for PCM (Pulse Code Modulation) audio reduces to the sample rate.




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

For video streams, this number is typically zero, although it can be nonzero if all video frames are the same size. For audio streams, this number should be the same as the <b>nBlockAlign</b> member of the <a href="https://msdn.microsoft.com/48871868-792a-4479-9e92-95306c25673a">WAVEFORMAT</a> or <a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure describing the audio.


### -field rcFrame

Dimensions of the video destination rectangle. The values represent the coordinates of upper left corner, the height, and the width of the rectangle.


### -field dwEditCount

Number of times the stream has been edited. The stream handler maintains this count.


### -field dwFormatChangeCount

Number of times the stream format has changed. The stream handler maintains this count.


### -field szName

Null-terminated string containing a description of the stream.


## -see-also




<a href="https://msdn.microsoft.com/573e24fa-876d-4ce9-be23-d5e448a53e20">AVIFile Functions and Macros</a>



<a href="https://msdn.microsoft.com/2b7cdbb6-8c53-49ad-a171-b58357531887">AVIFile Structures</a>



<a href="https://msdn.microsoft.com/c09dc3f0-e1bc-4643-9b27-bcf1dcc5710c">PCMWAVEFORMAT</a>



<a href="https://msdn.microsoft.com/48871868-792a-4479-9e92-95306c25673a">WAVEFORMAT</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a>



<a href="https://msdn.microsoft.com/616c3b43-9305-49c1-bc46-2e1256647c7d">mmioFOURCC</a>
 

 

