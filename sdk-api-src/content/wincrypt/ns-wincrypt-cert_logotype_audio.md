---
UID: NS:wincrypt._CERT_LOGOTYPE_AUDIO
title: CERT_LOGOTYPE_AUDIO (wincrypt.h)
description: Contains information about an audio logotype.
helpviewer_keywords: ["*PCERT_LOGOTYPE_AUDIO","CERT_LOGOTYPE_AUDIO","CERT_LOGOTYPE_AUDIO structure [Security]","PCERT_LOGOTYPE_AUDIO","PCERT_LOGOTYPE_AUDIO structure pointer [Security]","security.cert_logotype_audio","wincrypt/CERT_LOGOTYPE_AUDIO","wincrypt/PCERT_LOGOTYPE_AUDIO"]
old-location: security\cert_logotype_audio.htm
tech.root: security
ms.assetid: 97357faa-2720-4240-a3c3-77abdce8d86d
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_AUDIO, CERT_LOGOTYPE_AUDIO, CERT_LOGOTYPE_AUDIO structure [Security], PCERT_LOGOTYPE_AUDIO, PCERT_LOGOTYPE_AUDIO structure pointer [Security], security.cert_logotype_audio, wincrypt/CERT_LOGOTYPE_AUDIO, wincrypt/PCERT_LOGOTYPE_AUDIO'
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
req.typenames: CERT_LOGOTYPE_AUDIO, *PCERT_LOGOTYPE_AUDIO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_AUDIO
 - wincrypt/_CERT_LOGOTYPE_AUDIO
 - PCERT_LOGOTYPE_AUDIO
 - wincrypt/PCERT_LOGOTYPE_AUDIO
 - CERT_LOGOTYPE_AUDIO
 - wincrypt/CERT_LOGOTYPE_AUDIO
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
 - CERT_LOGOTYPE_AUDIO
---

# CERT_LOGOTYPE_AUDIO structure


## -description

The <b>CERT_LOGOTYPE_AUDIO</b> structure contains information about an audio logotype.

## -struct-fields

### -field LogotypeDetails

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_details">CERT_LOGOTYPE_DETAILS</a> structure that contains additional information about the audio data.

### -field pLogotypeAudioInfo

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_audio_info">CERT_LOGOTYPE_AUDIO_INFO</a> structure that contains the audio information.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_data">CERT_LOGOTYPE_DATA</a>