---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# mpeglayer3waveformat_tag structure


## -description



          The <b>MPEGLAYER3WAVEFORMAT</b> structure describes an MPEG Audio Layer-3 (MP3) audio format.
        


## -struct-fields




### -field wfx


<a href="https://msdn.microsoft.com/library/windows/hardware/ff538799">WAVEFORMATEX</a> structure that specifies the basic audio format. The <b>wFormatTag</b> member must be <b>WAVE_FORMAT_MPEGLAYER3</b>. The <b>cbSize</b> member must be at least 12. (For <b>cbSize</b>, you can use the constant <b>MPEGLAYER3_WFX_EXTRA_BYTES</b>, defined in the Mmreg.h.)


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




<a href="https://msdn.microsoft.com/378f6f43-5c05-4ae4-be24-956f9fc0cacf">DirectShow Structures</a>
 

 

