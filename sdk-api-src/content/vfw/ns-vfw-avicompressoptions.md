---
UID: NS:vfw.AVICOMPRESSOPTIONS
title: AVICOMPRESSOPTIONS
author: windows-sdk-content
description: The AVICOMPRESSOPTIONS structure contains information about a stream and how it is compressed and saved. This structure passes data to the AVIMakeCompressedStream function (or the AVISave function, which uses AVIMakeCompressedStream).
old-location: multimedia\avicompressoptions.htm
tech.root: Multimedia
ms.assetid: 8084adc3-792f-4a6c-b407-51e0e435e629
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: "*LPAVICOMPRESSOPTIONS, AVICOMPRESSF_DATARATE, AVICOMPRESSF_INTERLEAVE, AVICOMPRESSF_KEYFRAMES, AVICOMPRESSF_VALID, AVICOMPRESSOPTIONS, AVICOMPRESSOPTIONS structure [Windows Multimedia], _win32_AVICOMPRESSOPTIONS_str, multimedia.avicompressoptions, streamtypeAUDIO, streamtypeMIDI, streamtypeTEXT, streamtypeVIDEO, vfw/AVICOMPRESSOPTIONS"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Vfw.h
api_name:
 - AVICOMPRESSOPTIONS
product: Windows
targetos: Windows
req.typenames: AVICOMPRESSOPTIONS, *LPAVICOMPRESSOPTIONS
req.redist: 
---

# AVICOMPRESSOPTIONS structure


## -description



The <b>AVICOMPRESSOPTIONS</b> structure contains information about a stream and how it is compressed and saved. This structure passes data to the <a href="https://msdn.microsoft.com/63279d7e-0e64-4708-a29c-60d5fdf75cb2">AVIMakeCompressedStream</a> function (or the <a href="https://msdn.microsoft.com/44200871-541c-4d67-ba12-61af06da8788">AVISave</a> function, which uses <b>AVIMakeCompressedStream</b>).




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

Four-character code for the compressor handler that will compress this video stream when it is saved (for example, <a href="https://msdn.microsoft.com/616c3b43-9305-49c1-bc46-2e1256647c7d">mmioFOURCC</a> ('M','S','V','C')). This member is not used for audio streams.


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
Uses the data in this structure to set the default compression values for <a href="https://msdn.microsoft.com/6141272f-a815-4ba8-bc6b-41751d6e0104">AVISaveOptions</a>. If an empty structure is passed and this flag is not set, some defaults will be chosen.

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



<a href="https://msdn.microsoft.com/2b7cdbb6-8c53-49ad-a171-b58357531887">AVIFile Structures</a>



<a href="https://msdn.microsoft.com/63279d7e-0e64-4708-a29c-60d5fdf75cb2">AVIMakeCompressedStream</a>



<a href="https://msdn.microsoft.com/44200871-541c-4d67-ba12-61af06da8788">AVISave</a>



<a href="https://msdn.microsoft.com/6141272f-a815-4ba8-bc6b-41751d6e0104">AVISaveOptions</a>



<a href="https://msdn.microsoft.com/616c3b43-9305-49c1-bc46-2e1256647c7d">mmioFOURCC</a>
 

 

