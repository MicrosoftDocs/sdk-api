---
UID: NS:vfw.AVICOMPRESSOPTIONS
title: AVICOMPRESSOPTIONS (vfw.h)
description: The AVICOMPRESSOPTIONS structure contains information about a stream and how it is compressed and saved. This structure passes data to the AVIMakeCompressedStream function (or the AVISave function, which uses AVIMakeCompressedStream).
helpviewer_keywords: ["*LPAVICOMPRESSOPTIONS","AVICOMPRESSF_DATARATE","AVICOMPRESSF_INTERLEAVE","AVICOMPRESSF_KEYFRAMES","AVICOMPRESSF_VALID","AVICOMPRESSOPTIONS","AVICOMPRESSOPTIONS structure [Windows Multimedia]","_win32_AVICOMPRESSOPTIONS_str","multimedia.avicompressoptions","streamtypeAUDIO","streamtypeMIDI","streamtypeTEXT","streamtypeVIDEO","vfw/AVICOMPRESSOPTIONS"]
old-location: multimedia\avicompressoptions.htm
tech.root: Multimedia
ms.assetid: 8084adc3-792f-4a6c-b407-51e0e435e629
ms.date: 12/05/2018
ms.keywords: '*LPAVICOMPRESSOPTIONS, AVICOMPRESSF_DATARATE, AVICOMPRESSF_INTERLEAVE, AVICOMPRESSF_KEYFRAMES, AVICOMPRESSF_VALID, AVICOMPRESSOPTIONS, AVICOMPRESSOPTIONS structure [Windows Multimedia], _win32_AVICOMPRESSOPTIONS_str, multimedia.avicompressoptions, streamtypeAUDIO, streamtypeMIDI, streamtypeTEXT, streamtypeVIDEO, vfw/AVICOMPRESSOPTIONS'
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
req.typenames: AVICOMPRESSOPTIONS, *LPAVICOMPRESSOPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - LPAVICOMPRESSOPTIONS
 - vfw/LPAVICOMPRESSOPTIONS
 - AVICOMPRESSOPTIONS
 - vfw/AVICOMPRESSOPTIONS
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
 - AVICOMPRESSOPTIONS
---

# AVICOMPRESSOPTIONS structure


## -description

The <b>AVICOMPRESSOPTIONS</b> structure contains information about a stream and how it is compressed and saved. This structure passes data to the <a href="/windows/desktop/api/vfw/nf-vfw-avimakecompressedstream">AVIMakeCompressedStream</a> function (or the <a href="/windows/desktop/api/vfw/nf-vfw-avisavea">AVISave</a> function, which uses <b>AVIMakeCompressedStream</b>).

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

Four-character code for the compressor handler that will compress this video stream when it is saved (for example, <a href="/windows/desktop/api/vfw/nf-vfw-mmiofourcc">mmioFOURCC</a> ('M','S','V','C')). This member is not used for audio streams.

### -field dwKeyFrameEvery

Maximum period between video key frames. This member is used only if the AVICOMPRESSF_KEYFRAMES flag is set; otherwise every video frame is a key frame.

### -field dwQuality

Quality value passed to a video compressor. This member is not used for an audio compressor.

### -field dwBytesPerSecond

Video compressor data rate. This member is used only if the AVICOMPRESSF_DATARATE flag is set.

### -field dwFlags

Flags used for compression. The following values are defined:

<table>
<tr>
<th>Name</th>
<th>Description</th>
</tr>
<tr>
<td width="40%"><a id="AVICOMPRESSF_DATARATE"></a><a id="avicompressf_datarate"></a><dl>
<dt><b>AVICOMPRESSF_DATARATE</b></dt>
</dl>
</td>
<td width="60%">
Compresses this video stream using the data rate specified in <b>dwBytesPerSecond</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="AVICOMPRESSF_INTERLEAVE"></a><a id="avicompressf_interleave"></a><dl>
<dt><b>AVICOMPRESSF_INTERLEAVE</b></dt>
</dl>
</td>
<td width="60%">
Interleaves this stream every <b>dwInterleaveEvery</b> frames with respect to the first stream.

</td>
</tr>
<tr>
<td width="40%"><a id="AVICOMPRESSF_KEYFRAMES"></a><a id="avicompressf_keyframes"></a><dl>
<dt><b>AVICOMPRESSF_KEYFRAMES</b></dt>
</dl>
</td>
<td width="60%">
Saves this video stream with key frames at least every <b>dwKeyFrameEvery</b> frames. By default, every frame will be a key frame.

</td>
</tr>
<tr>
<td width="40%"><a id="AVICOMPRESSF_VALID"></a><a id="avicompressf_valid"></a><dl>
<dt><b>AVICOMPRESSF_VALID</b></dt>
</dl>
</td>
<td width="60%">
Uses the data in this structure to set the default compression values for <a href="/windows/desktop/api/vfw/nf-vfw-avisaveoptions">AVISaveOptions</a>. If an empty structure is passed and this flag is not set, some defaults will be chosen.

</td>
</tr>
</table>

### -field lpFormat

Pointer to a structure defining the data format. For an audio stream, this is an <b>LPWAVEFORMAT</b> structure.

### -field cbFormat

Size, in bytes, of the data referenced by <b>lpFormat</b>.

### -field lpParms

Video-compressor-specific data; used internally.

### -field cbParms

Size, in bytes, of the data referenced by <b>lpParms</b>

### -field dwInterleaveEvery

Interleave factor for interspersing stream data with data from the first stream. Used only if the AVICOMPRESSF_INTERLEAVE flag is set.

## -see-also

AVIFile Functions and Macros



<a href="/windows/desktop/Multimedia/avifile-structures">AVIFile Structures</a>



<a href="/windows/desktop/api/vfw/nf-vfw-avimakecompressedstream">AVIMakeCompressedStream</a>



<a href="/windows/desktop/api/vfw/nf-vfw-avisavea">AVISave</a>



<a href="/windows/desktop/api/vfw/nf-vfw-avisaveoptions">AVISaveOptions</a>



<a href="/windows/desktop/api/vfw/nf-vfw-mmiofourcc">mmioFOURCC</a>

