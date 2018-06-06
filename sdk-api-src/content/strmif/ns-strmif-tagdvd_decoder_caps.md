---
UID: NS:strmif.tagDVD_DECODER_CAPS
title: tagDVD_DECODER_CAPS
author: windows-sdk-content
description: The DVD_DECODER_CAPS structure indicates the capabilities of a DVD decoder.
old-location: dshow\dvd_decoder_caps.htm
old-project: DirectShow
ms.assetid: 7bfe5922-5d84-4ec8-87a0-e9bad102508b
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: DVD_AUDIO_CAPS_AC3, DVD_AUDIO_CAPS_DTS, DVD_AUDIO_CAPS_LPCM, DVD_AUDIO_CAPS_MPEG2, DVD_AUDIO_CAPS_SDDS, DVD_DECODER_CAPS, DVD_DECODER_CAPS structure [DirectShow], DVD_DECODER_CAPSStructure, dshow.dvd_decoder_caps, strmif/DVD_DECODER_CAPS, tagDVD_DECODER_CAPS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: DVD_DECODER_CAPS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - DVD_DECODER_CAPS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# tagDVD_DECODER_CAPS structure


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




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>



<a href="https://msdn.microsoft.com/cfaf475c-336a-492f-b5a8-c49c21e5392d">IDvdInfo2::GetDecoderCaps</a>
 

 

