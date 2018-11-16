---
UID: NS:wincrypt._CERT_LOGOTYPE_AUDIO
title: "_CERT_LOGOTYPE_AUDIO"
author: windows-sdk-content
description: Contains information about an audio logotype.
old-location: security\cert_logotype_audio.htm
tech.root: SecCrypto
ms.assetid: 97357faa-2720-4240-a3c3-77abdce8d86d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PCERT_LOGOTYPE_AUDIO, CERT_LOGOTYPE_AUDIO, CERT_LOGOTYPE_AUDIO structure [Security], PCERT_LOGOTYPE_AUDIO, PCERT_LOGOTYPE_AUDIO structure pointer [Security], _CERT_LOGOTYPE_AUDIO, security.cert_logotype_audio, wincrypt/CERT_LOGOTYPE_AUDIO, wincrypt/PCERT_LOGOTYPE_AUDIO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_LOGOTYPE_AUDIO
product: Windows
targetos: Windows
req.typenames: CERT_LOGOTYPE_AUDIO, *PCERT_LOGOTYPE_AUDIO
req.redist: 
---

# _CERT_LOGOTYPE_AUDIO structure


## -description


The <b>CERT_LOGOTYPE_AUDIO</b> structure contains information about an audio logotype.


## -struct-fields




### -field LogotypeDetails

A <a href="https://msdn.microsoft.com/cde420a8-c755-4c45-ab81-4897b08d9dd6">CERT_LOGOTYPE_DETAILS</a> structure that contains additional information about the audio data.


### -field pLogotypeAudioInfo

The address of a <a href="https://msdn.microsoft.com/7a12447b-1561-4fbc-8984-d28555a13159">CERT_LOGOTYPE_AUDIO_INFO</a> structure that contains the audio information.


## -see-also




<a href="https://msdn.microsoft.com/f170dd48-a0f4-45e0-b5b8-a5f446d1a86e">CERT_LOGOTYPE_DATA</a>
 

 

