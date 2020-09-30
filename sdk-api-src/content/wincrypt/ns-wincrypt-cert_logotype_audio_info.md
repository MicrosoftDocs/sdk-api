---
UID: NS:wincrypt._CERT_LOGOTYPE_AUDIO_INFO
title: CERT_LOGOTYPE_AUDIO_INFO (wincrypt.h)
description: Contains more detailed information about an audio logotype.
helpviewer_keywords: ["*PCERT_LOGOTYPE_AUDIO_INFO","CERT_LOGOTYPE_AUDIO_INFO","CERT_LOGOTYPE_AUDIO_INFO structure [Security]","PCERT_LOGOTYPE_AUDIO_INFO","PCERT_LOGOTYPE_AUDIO_INFO structure pointer [Security]","security.cert_logotype_audio_info","wincrypt/CERT_LOGOTYPE_AUDIO_INFO","wincrypt/PCERT_LOGOTYPE_AUDIO_INFO"]
old-location: security\cert_logotype_audio_info.htm
tech.root: security
ms.assetid: 7a12447b-1561-4fbc-8984-d28555a13159
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_AUDIO_INFO, CERT_LOGOTYPE_AUDIO_INFO, CERT_LOGOTYPE_AUDIO_INFO structure [Security], PCERT_LOGOTYPE_AUDIO_INFO, PCERT_LOGOTYPE_AUDIO_INFO structure pointer [Security], security.cert_logotype_audio_info, wincrypt/CERT_LOGOTYPE_AUDIO_INFO, wincrypt/PCERT_LOGOTYPE_AUDIO_INFO'
req.header: wincrypt.h
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
targetos: Windows
req.typenames: CERT_LOGOTYPE_AUDIO_INFO, *PCERT_LOGOTYPE_AUDIO_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_AUDIO_INFO
 - wincrypt/_CERT_LOGOTYPE_AUDIO_INFO
 - PCERT_LOGOTYPE_AUDIO_INFO
 - wincrypt/PCERT_LOGOTYPE_AUDIO_INFO
 - CERT_LOGOTYPE_AUDIO_INFO
 - wincrypt/CERT_LOGOTYPE_AUDIO_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_LOGOTYPE_AUDIO_INFO
---

# CERT_LOGOTYPE_AUDIO_INFO structure


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

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_audio">CERT_LOGOTYPE_AUDIO</a>