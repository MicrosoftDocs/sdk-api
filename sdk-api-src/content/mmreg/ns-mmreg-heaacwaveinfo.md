---
UID: NS:mmreg.heaacwaveinfo_tag
title: HEAACWAVEINFO (mmreg.h)
description: Contains format data for an Advanced Audio Coding (AAC) or High-Efficiency Advanced Audio Coding (HE-AAC) stream.helpviewer_keywords: ["*LPHEAACWAVEINFO","*NPHEAACWAVEINFO","*PHEAACWAVEINFO","HEAACWAVEINFO","HEAACWAVEINFO structure [DirectShow]","PHEAACWAVEINFO","PHEAACWAVEINFO structure pointer [DirectShow]","dshow.heaacwaveinfo","heaacwaveinfo_tag","mmreg/HEAACWAVEINFO","mmreg/PHEAACWAVEINFO"]
old-location: dshow\heaacwaveinfo.htm
tech.root: DirectShow
ms.assetid: a9b888fb-b4a5-44c3-a715-687cc751063d
ms.date: 12/05/2018
ms.keywords: '*LPHEAACWAVEINFO, *NPHEAACWAVEINFO, *PHEAACWAVEINFO, HEAACWAVEINFO, HEAACWAVEINFO structure [DirectShow], PHEAACWAVEINFO, PHEAACWAVEINFO structure pointer [DirectShow], dshow.heaacwaveinfo, heaacwaveinfo_tag, mmreg/HEAACWAVEINFO, mmreg/PHEAACWAVEINFO'
f1_keywords:
- mmreg/HEAACWAVEINFO
dev_langs:
- c++
req.header: mmreg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
- mmreg.h
api_name:
- HEAACWAVEINFO
targetos: Windows
req.typenames: HEAACWAVEINFO
req.redist: 
ms.custom: 19H1
---

# HEAACWAVEINFO structure


## -description


Contains format data for an Advanced Audio Coding (AAC) or High-Efficiency Advanced Audio Coding (HE-AAC) stream.


## -struct-fields




### -field wfx

A <b>WAVEFORMATEX</b> structure that describes the core AAC stream,
 without SBR or PS extensions. See Remarks.




### -field wPayloadType

The payload type.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The stream contains raw_data_block elements only.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Audio Data Transport Stream (ADTS). The stream contains an adts_sequence, as defined by MPEG-2.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Audio Data Interchange Format (ADIF). The stream contains an adif_sequence, as defined by MPEG-2.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The stream contains an MPEG-4 audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).


</td>
</tr>
</table>
 


### -field wAudioProfileLevelIndication

Contains the value of the <b>audioProfileLevelIndication</b> field, as defined by ISO/IEC 14496-3 (MPEG-4 Audio). If the value is unknown, set this member to zero or 0xFE ("no audio profile specified").


### -field wStructType

Defines the data that follows this structure. Currently the following value is defined.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The data that follows the <b>HEAACWAVEINFO</b> structure contains the value of AudioSpecificConfig(), as defined by ISO/IEC 14496-3. 

The size of the data is <code>wfx.cbSize - sizeof(HEAACWAVEINFO) + sizeof(WAVEFORMATEX)</code>. If the size is greater than zero, you can access the data by casting the <b>HEAACWAVEINFO</b> structure to a <a href="https://docs.microsoft.com/windows/desktop/api/mmreg/ns-mmreg-heaacwaveformat">HEAACWAVEFORMAT</a> structure.

</td>
</tr>
</table>
 

All other values for this member are reserved.


### -field wReserved1

Reserved. Set to zero.


### -field dwReserved2

Reserved. Set to zero.


## -remarks



This format structure is used to describe MPEG-2 AAC and MPEG-4 HE-AAC streams, including HE-AAC version 1 and HE-AAC version 2.

The <b>WAVEFORMATEX</b> structure defined in the <b>wfx</b> member contains the following values.



<table>
<tr>
<th>Member</th>
<th>Description</th>
</tr>
<tr>
<td><b>wFormatTag</b></td>
<td>Must be <b>WAVE_FORMAT_MPEG_HEAAC</b> (0x1610).</td>
</tr>
<tr>
<td><b>nChannels</b></td>
<td>The number of channels in the core AAC stream, including the low frequency (LFE) channel, if present.
 If parametric stereo (PS) 
 is used, the value might differ from the number of channels in the decoded stream. If unknown, set to zero.</td>
</tr>
<tr>
<td><b>nSamplesPerSec</b></td>
<td>The sampling rate of the core AAC stream. The value must be one of the supported
 sampling rates, from 8000 to 96000 Hz, defined in MPEG-2.  If spectral band replication (SBR) is used, the value might differ from the sampling rate of the decoded stream. If unknown, set to zero.</td>
</tr>
<tr>
<td><b>nAvgBytesPerSec</b></td>
<td>The average bytes per second, calculated from the average bit rate of
 the compressed stream. If unknown, set to zero.</td>
</tr>
<tr>
<td><b>nBlockAlign</b></td>
<td>Set to 1.</td>
</tr>
<tr>
<td><b>wBitsPerSample</b></td>
<td>The desired number of bits per sample in the decoded PCM audio stream. If unknown, set to zero.</td>
</tr>
<tr>
<td><b>cbSize</b></td>
<td>Specifies the size, in bytes, of the format data after the <b>WAVEFORMATEX</b> structure.</td>
</tr>
</table>
 





