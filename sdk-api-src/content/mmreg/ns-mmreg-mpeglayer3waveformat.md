---
UID: NS:mmreg.mpeglayer3waveformat_tag
title: MPEGLAYER3WAVEFORMAT (mmreg.h)
description: The MPEGLAYER3WAVEFORMAT structure describes an MPEG Audio Layer-3 (MP3) audio format.
helpviewer_keywords: ["*LPMPEGLAYER3WAVEFORMAT","*NPMPEGLAYER3WAVEFORMAT","*PMPEGLAYER3WAVEFORMAT","MPEGLAYER3WAVEFORMAT","MPEGLAYER3WAVEFORMAT structure [DirectShow]","MPEGLAYER3WAVEFORMATStructure","MPEGLAYER3_FLAG_PADDING_ISO","MPEGLAYER3_FLAG_PADDING_OFF","MPEGLAYER3_FLAG_PADDING_ON","dshow.mpeglayer3waveformat","mmreg/MPEGLAYER3WAVEFORMAT","mpeglayer3waveformat_tag"]
old-location: dshow\mpeglayer3waveformat.htm
tech.root: dshow
ms.assetid: eca403a0-01a2-4290-951f-a7d516a58b9e
ms.date: 4/26/2023
ms.keywords: '*LPMPEGLAYER3WAVEFORMAT, *NPMPEGLAYER3WAVEFORMAT, *PMPEGLAYER3WAVEFORMAT, MPEGLAYER3WAVEFORMAT, MPEGLAYER3WAVEFORMAT structure [DirectShow], MPEGLAYER3WAVEFORMATStructure, MPEGLAYER3_FLAG_PADDING_ISO, MPEGLAYER3_FLAG_PADDING_OFF, MPEGLAYER3_FLAG_PADDING_ON, dshow.mpeglayer3waveformat, mmreg/MPEGLAYER3WAVEFORMAT, mpeglayer3waveformat_tag'
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
req.typenames: MPEGLAYER3WAVEFORMAT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - mpeglayer3waveformat_tag
 - mmreg/mpeglayer3waveformat_tag
 - MPEGLAYER3WAVEFORMAT
 - mmreg/MPEGLAYER3WAVEFORMAT
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
 - MPEGLAYER3WAVEFORMAT
---

# MPEGLAYER3WAVEFORMAT structure


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <b>MPEGLAYER3WAVEFORMAT</b> structure describes an MPEG Audio Layer-3 (MP3) audio format.

## -struct-fields

### -field wfx

<a href="/previous-versions/dd757713(v=vs.85)">WAVEFORMATEX</a> structure that specifies the basic audio format. The <b>wFormatTag</b> member must be <b>WAVE_FORMAT_MPEGLAYER3</b>. The <b>cbSize</b> member must be at least 12. (For <b>cbSize</b>, you can use the constant <b>MPEGLAYER3_WFX_EXTRA_BYTES</b>, defined in the Mmreg.h.)

### -field wID

Set this structure member to <b>MPEGLAYER3_ID_MPEG</b>.

### -field fdwFlags

Indicates whether padding is used to adjust the average bitrate to the sampling rate. Use one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MPEGLAYER3_FLAG_PADDING_ISO"></a><a id="mpeglayer3_flag_padding_iso"></a><dl>
<dt><b>MPEGLAYER3_FLAG_PADDING_ISO</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
Insert padding as needed to achieve the stated average bitrate.

</td>
</tr>
<tr>
<td width="40%"><a id="MPEGLAYER3_FLAG_PADDING_ON"></a><a id="mpeglayer3_flag_padding_on"></a><dl>
<dt><b>MPEGLAYER3_FLAG_PADDING_ON</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Always insert padding. The average bit rate may be higher than stated.

</td>
</tr>
<tr>
<td width="40%"><a id="MPEGLAYER3_FLAG_PADDING_OFF"></a><a id="mpeglayer3_flag_padding_off"></a><dl>
<dt><b>MPEGLAYER3_FLAG_PADDING_OFF</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Never insert padding. The average bit rate may be lower than stated.

</td>
</tr>
</table>

### -field nBlockSize

Block size in bytes. This value equals the frame length in bytes x <b>nFramesPerBlock</b>. For MP3 audio, the frame length is calculated as follows: 144 x (bitrate / sample rate) + padding.

### -field nFramesPerBlock

Number of audio frames per block.

### -field nCodecDelay

Encoder delay in samples. If you do not know this value, set this structure member to zero.

## -see-also

<a href="/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>