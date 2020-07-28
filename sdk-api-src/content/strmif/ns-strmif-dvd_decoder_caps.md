---
UID: NS:strmif.tagDVD_DECODER_CAPS
title: DVD_DECODER_CAPS (strmif.h)
description: The DVD_DECODER_CAPS structure indicates the capabilities of a DVD decoder.
helpviewer_keywords: ["DVD_AUDIO_CAPS_AC3","DVD_AUDIO_CAPS_DTS","DVD_AUDIO_CAPS_LPCM","DVD_AUDIO_CAPS_MPEG2","DVD_AUDIO_CAPS_SDDS","DVD_DECODER_CAPS","DVD_DECODER_CAPS structure [DirectShow]","DVD_DECODER_CAPSStructure","dshow.dvd_decoder_caps","strmif/DVD_DECODER_CAPS"]
old-location: dshow\dvd_decoder_caps.htm
tech.root: dshow
ms.assetid: 7bfe5922-5d84-4ec8-87a0-e9bad102508b
ms.date: 12/05/2018
ms.keywords: DVD_AUDIO_CAPS_AC3, DVD_AUDIO_CAPS_DTS, DVD_AUDIO_CAPS_LPCM, DVD_AUDIO_CAPS_MPEG2, DVD_AUDIO_CAPS_SDDS, DVD_DECODER_CAPS, DVD_DECODER_CAPS structure [DirectShow], DVD_DECODER_CAPSStructure, dshow.dvd_decoder_caps, strmif/DVD_DECODER_CAPS
f1_keywords:
- strmif/DVD_DECODER_CAPS
dev_langs:
- c++
req.header: strmif.h
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
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- strmif.h
api_name:
- DVD_DECODER_CAPS
targetos: Windows
req.typenames: DVD_DECODER_CAPS
req.redist: 
ms.custom: 19H1
---

# DVD_DECODER_CAPS structure


## -description



The <code>DVD_DECODER_CAPS</code> structure indicates the capabilities of a DVD decoder.




## -struct-fields




### -field dwSize

Size of this structure.


### -field dwAudioCaps

Bitwise <b>OR</b> of flags indicating which audio formats are supported. The following flags are defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="DVD_AUDIO_CAPS_AC3"></a><a id="dvd_audio_caps_ac3"></a><dl>
<dt><b>DVD_AUDIO_CAPS_AC3</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Dolby Digital (AC3).

</td>
</tr>
<tr>
<td width="40%"><a id="DVD_AUDIO_CAPS_MPEG2"></a><a id="dvd_audio_caps_mpeg2"></a><dl>
<dt><b>DVD_AUDIO_CAPS_MPEG2</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
MPEG-2 audio.

</td>
</tr>
<tr>
<td width="40%"><a id="DVD_AUDIO_CAPS_LPCM"></a><a id="dvd_audio_caps_lpcm"></a><dl>
<dt><b>DVD_AUDIO_CAPS_LPCM</b></dt>
<dt>0x00000004</dt>
</dl>
</td>
<td width="60%">
Linear pulse code modulation (LPCM).

</td>
</tr>
<tr>
<td width="40%"><a id="DVD_AUDIO_CAPS_DTS"></a><a id="dvd_audio_caps_dts"></a><dl>
<dt><b>DVD_AUDIO_CAPS_DTS</b></dt>
<dt>0x00000008</dt>
</dl>
</td>
<td width="60%">
DTS audio.

</td>
</tr>
<tr>
<td width="40%"><a id="DVD_AUDIO_CAPS_SDDS"></a><a id="dvd_audio_caps_sdds"></a><dl>
<dt><b>DVD_AUDIO_CAPS_SDDS</b></dt>
<dt>0x00000010</dt>
</dl>
</td>
<td width="60%">
Sony Dynamic Digital Sound (SDDS) audio.

</td>
</tr>
</table>
 


### -field dFwdMaxRateVideo

Maximum video data rate in forward direction.


### -field dFwdMaxRateAudio

Maximum audio data rate in forward direction.


### -field dFwdMaxRateSP

Maximum subpicture data rate in forward direction.


### -field dBwdMaxRateVideo

Maximum video data rate in reverse direction. (0 if decoder does not support the smooth reverse mechanism.)


### -field dBwdMaxRateAudio

Maximum audio data rate in reverse direction. (0 if decoder does not support the smooth reverse mechanism.)


### -field dBwdMaxRateSP

Maximum subpicture data rate in reverse direction. (0 if decoder does not support the smooth reverse mechanism.)


### -field dwRes1

Reserved for future use.


### -field dwRes2

Reserved for future use.


### -field dwRes3

Reserved for future use.


### -field dwRes4

Reserved for future use.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/DirectShow/directshow-structures">DirectShow Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-idvdinfo2-getdecodercaps">IDvdInfo2::GetDecoderCaps</a>
 

 

