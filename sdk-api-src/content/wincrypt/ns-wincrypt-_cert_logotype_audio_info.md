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

# _CERT_LOGOTYPE_AUDIO_INFO structure


## -description


The <b>CERT_LOGOTYPE_AUDIO_INFO</b> structure contains more detailed information about an audio logotype.


## -struct-fields




### -field dwFileSize

The size, in octets, of the audio.


### -field dwPlayTime

The length of play time, in milliseconds, of the audio.


### -field dwChannels

The number of channels in the audio file. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The audio file is monaural.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The audio file is stereo.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The audio file contains four channels.

</td>
</tr>
</table>
 


### -field dwSampleRate

The sample rate of the audio, in samples per second. This member is optional and may be zero.


### -field pwszLanguage

The address of a null-terminated IA5 string that contains the RFC 3066 language identifier that specifies the language of the audio. This member is optional and may be <b>NULL</b>.


## -see-also




<a href="https://msdn.microsoft.com/97357faa-2720-4240-a3c3-77abdce8d86d">CERT_LOGOTYPE_AUDIO</a>
 

 

