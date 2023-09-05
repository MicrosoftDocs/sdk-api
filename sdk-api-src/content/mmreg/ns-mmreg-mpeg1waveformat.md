---
UID: NS:mmreg.mpeg1waveformat_tag
title: MPEG1WAVEFORMAT (mmreg.h)
description: The MPEG1WAVEFORMAT structure describes the format of MPEG-1 audio data.
helpviewer_keywords: ["*LPMPEG1WAVEFORMAT","*NPMPEG1WAVEFORMAT","*PMPEG1WAVEFORMAT","ACM_MPEG_COPYRIGHT","ACM_MPEG_DUALCHANNEL","ACM_MPEG_ID_MPEG1","ACM_MPEG_JOINTSTEREO","ACM_MPEG_LAYER1","ACM_MPEG_LAYER2","ACM_MPEG_LAYER3","ACM_MPEG_ORIGINALHOME","ACM_MPEG_PRIVATEBIT","ACM_MPEG_PROTECTIONBIT","ACM_MPEG_SINGLECHANNEL","ACM_MPEG_STEREO","MPEG1WAVEFORMAT","MPEG1WAVEFORMAT structure [DirectShow]","dshow.mpeg1waveformat","mmreg/MPEG1WAVEFORMAT","mpeg1waveformat_tag"]
old-location: dshow\mpeg1waveformat.htm
tech.root: dshow
ms.assetid: c9357f72-f101-434a-b7ae-183e78239e9c
ms.date: 4/26/2023
ms.keywords: '*LPMPEG1WAVEFORMAT, *NPMPEG1WAVEFORMAT, *PMPEG1WAVEFORMAT, ACM_MPEG_COPYRIGHT, ACM_MPEG_DUALCHANNEL, ACM_MPEG_ID_MPEG1, ACM_MPEG_JOINTSTEREO, ACM_MPEG_LAYER1, ACM_MPEG_LAYER2, ACM_MPEG_LAYER3, ACM_MPEG_ORIGINALHOME, ACM_MPEG_PRIVATEBIT, ACM_MPEG_PROTECTIONBIT, ACM_MPEG_SINGLECHANNEL, ACM_MPEG_STEREO, MPEG1WAVEFORMAT, MPEG1WAVEFORMAT structure [DirectShow], dshow.mpeg1waveformat, mmreg/MPEG1WAVEFORMAT, mpeg1waveformat_tag'
req.header: mmreg.h
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
req.typenames: MPEG1WAVEFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mpeg1waveformat_tag
 - mmreg/mpeg1waveformat_tag
 - MPEG1WAVEFORMAT
 - mmreg/MPEG1WAVEFORMAT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mmreg.h
api_name:
 - MPEG1WAVEFORMAT
---

# MPEG1WAVEFORMAT structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>MPEG1WAVEFORMAT</code> structure describes the format of MPEG-1 audio data.

## -struct-fields

### -field wfx

<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that contains information about the audio format. See Remarks.

### -field fwHeadLayer

Specifies the MPEG audio layer, as defined by the following constants:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_LAYER1"></a><a id="acm_mpeg_layer1"></a><dl>
<dt><b>ACM_MPEG_LAYER1</b></dt>
</dl>
</td>
<td width="60%">
Layer 1

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_LAYER2"></a><a id="acm_mpeg_layer2"></a><dl>
<dt><b>ACM_MPEG_LAYER2</b></dt>
</dl>
</td>
<td width="60%">
Layer 2

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_LAYER3"></a><a id="acm_mpeg_layer3"></a><dl>
<dt><b>ACM_MPEG_LAYER3</b></dt>
</dl>
</td>
<td width="60%">
Layer 3

</td>
</tr>
</table>
 

Some MPEG streams may contain frames from more than one layer. If so, combine the flags with a bitwise <b>OR</b>.

### -field dwHeadBitrate

Specifies the bitrate, in bits per second. This value gives the actual bitrate, not the MPEG frame header code. If the bitrate is variable, or is a non-standard bitrate, set this field to zero.

### -field fwHeadMode

Specifies the stream mode, as defined by the following constants:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_STEREO"></a><a id="acm_mpeg_stereo"></a><dl>
<dt><b>ACM_MPEG_STEREO</b></dt>
</dl>
</td>
<td width="60%">
Stereo

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_JOINTSTEREO"></a><a id="acm_mpeg_jointstereo"></a><dl>
<dt><b>ACM_MPEG_JOINTSTEREO</b></dt>
</dl>
</td>
<td width="60%">
Joint stereo

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_DUALCHANNEL"></a><a id="acm_mpeg_dualchannel"></a><dl>
<dt><b>ACM_MPEG_DUALCHANNEL</b></dt>
</dl>
</td>
<td width="60%">
Dual channel

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_SINGLECHANNEL"></a><a id="acm_mpeg_singlechannel"></a><dl>
<dt><b>ACM_MPEG_SINGLECHANNEL</b></dt>
</dl>
</td>
<td width="60%">
Single channel

</td>
</tr>
</table>
 

Some MPEG streams may contain frames with different modes. If so, combine the flags with a bitwise OR.

### -field fwHeadModeExt

Specifies the mode extension for joint-stereo encoding:

<table>
<tr>
<th>Value</th>
<th>MPEG Frame Header Code</th>
<th>Layers 1 and 2</th>
<th>Layer 3</th>
</tr>
<tr>
<td>0x01</td>
<td>'00'</td>
<td>Intensity stereo in bands 4 to 31</td>
<td>Intensity stereo off; Middle/Side (MS) stereo off </td>
</tr>
<tr>
<td>0x02</td>
<td>'01'</td>
<td>Intensity stereo in bands 8 to 31</td>
<td>Intensity stereo on; MS stereo off </td>
</tr>
<tr>
<td>0x04</td>
<td>'10'</td>
<td>Intensity stereo in bands 12 to 31</td>
<td>Intensity stereo off; MS stereo on </td>
</tr>
<tr>
<td>0x08</td>
<td>'11'</td>
<td>Intensity stereo in bands 16 to 31</td>
<td>Intensity stereo off; MS stereo on </td>
</tr>
</table>
 

These values may be combined with a bitwise <b>OR</b>. In general, encoders will dynamically switch between extension modes according to the characteristics of the signal. Therefore, for normal joint-stereo encoding, set this field to 0x0F (the bitwise OR of all the flags). However, you can use this field to limit the encoder to a set of allowable encoding types.

This field applies only when <b>fwHeadMode</b> includes ACM_MPEG_JOINTSTEREO. For other modes, set this field to zero.

### -field wHeadEmphasis

Specifies the de-emphasis required by the decoder:

<table>
<tr>
<th>Value</th>
<th>MPEG Frame Header</th>
<th>Code De-emphasis Required </th>
</tr>
<tr>
<td>1</td>
<td>'00'</td>
<td>None </td>
</tr>
<tr>
<td>2</td>
<td>'01'</td>
<td>50/15 ms emphasis </td>
</tr>
<tr>
<td>3</td>
<td>'10'</td>
<td>Reserved </td>
</tr>
<tr>
<td>4</td>
<td>'11'</td>
<td>CCITT J.17 </td>
</tr>
</table>

### -field fwHeadFlags

Specifies a bitwise combination of zero or more of the following flags:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_PRIVATEBIT"></a><a id="acm_mpeg_privatebit"></a><dl>
<dt><b>ACM_MPEG_PRIVATEBIT</b></dt>
</dl>
</td>
<td width="60%">
Set the private bit.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_COPYRIGHT"></a><a id="acm_mpeg_copyright"></a><dl>
<dt><b>ACM_MPEG_COPYRIGHT</b></dt>
</dl>
</td>
<td width="60%">
Set the copyright bit. 

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_ORIGINALHOME"></a><a id="acm_mpeg_originalhome"></a><dl>
<dt><b>ACM_MPEG_ORIGINALHOME</b></dt>
</dl>
</td>
<td width="60%">
Set the original/home bit. 

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_PROTECTIONBIT"></a><a id="acm_mpeg_protectionbit"></a><dl>
<dt><b>ACM_MPEG_PROTECTIONBIT</b></dt>
</dl>
</td>
<td width="60%">
Set the protection bit, and insert a 16-bit error protection code into each frame.

</td>
</tr>
<tr>
<td width="40%"><a id="ACM_MPEG_ID_MPEG1"></a><a id="acm_mpeg_id_mpeg1"></a><dl>
<dt><b>ACM_MPEG_ID_MPEG1</b></dt>
</dl>
</td>
<td width="60%">
Set the ID bit to 1, defining the stream as an MPEG-1 audio stream.

</td>
</tr>
</table>
 

An encoder will use these flags to set the corresponding bits in the MPEG audio frame headers.

### -field dwPTSLow

Specifies the least significant 32 bits of the presentation time stamp (PTS) of the first frame of the audio stream.

### -field dwPTSHigh

Specifies the most significant bit of the PTS. The <b>dwPTSLow</b> and <b>dwPTSHigh</b> fields can be treated as a single 64-bit value.

## -remarks

For MPEG-1 audio, the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure defined in the <b>wfx</b> member must have the following values.

<table>
<tr>
<th>WAVEFORMATEX Member
            </th>
<th>Description
            </th>
</tr>
<tr>
<td><b>wFormatTag</b></td>
<td>Must be WAVE_FORMAT_MPEG</td>
</tr>
<tr>
<td><b>nChannels</b></td>
<td>1 for mono, 2 for stereo</td>
</tr>
<tr>
<td><b>nSamplesPerSec</b></td>
<td>Specifies the sampling frequency, if the sampling frequency is fixed. If it is variable, set this field to zero.</td>
</tr>
<tr>
<td><b>nAvgBytesPerSec</b></td>
<td>Specifies the average data rate. If variable bitrate encoding is used under layer 3, the value might not be a legal MPEG-1 bit rate.</td>
</tr>
<tr>
<td><b>nBlockAlign</b></td>
<td>For audio streams with a fixed audio frame length, this field specifies the length of the audio frame. If the frame length is variable, set this field to 1.If the sampling frequency is 32 kHz or 48 kHz and the bit rate is constant, the audio frame size is constant. In that case, calculate <b>nBlockAlign</b> as follows:

<ul>
<li>Layer 1: <code>4 * (int)(12 * bitrate / sampling frequency)</code></li>
<li>Layers 2 and 3: <code>(int)(144 * bitrate / sampling frequency)</code></li>
</ul>
If the bit rate is variable or the sampling frequency is 44.1 kHz, the audio frame size is not constant and <b>nBlockAlign</b> should be 1.

</td>
</tr>
<tr>
<td><b>wBitsPerSample</b></td>
<td>Not used; set to zero.</td>
</tr>
<tr>
<td><b>cbSize</b></td>
<td>Specifies the size of the format data after the <a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure, in bytes. For the standard <b>MPEG1WAVEFORMAT</b> structure, this value is 22 bytes.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="/windows/desktop/DirectShow/mpeg-1-media-types">MPEG-1 Media Types</a>