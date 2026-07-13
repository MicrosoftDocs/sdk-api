---
UID: NN:audioengineextensionapo.IAudioProcessingObjectPreferredFormatSupport
tech.root: audio
title: IAudioProcessingObjectPreferredFormatSupport
ms.date: 08/28/2023
targetos: Windows
description: This interface is implemented by APOs to enable them to specify preferred input or output formats.
prerelease: false
req.assembly: 
req.construct-type: iface
req.ddi-compliance: 
req.header: audioengineextensionapo.h
req.idl: 
req.include-header: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 11, version 23H2
req.target-min-winversvr: 
req.target-type: 
req.unicode-ansi: 
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - audioengineextensionapo.h
api_name:
 - IAudioProcessingObjectPreferredFormatSupport
f1_keywords:
 - IAudioProcessingObjectPreferredFormatSupport
 - audioengineextensionapo/IAudioProcessingObjectPreferredFormatSupport
dev_langs:
 - c++
helpviewer_keywords:
 - IAudioProcessingObjectPreferredFormatSupport
---

## -description

This interface is implemented by APOs to enable them to specify preferred input or output formats. This allows APOs to declare a preferred format that may be different from the endpoint format. For example, this preferred value is returned when clients call [IAudioClient::GetMixFormat](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-getmixformat).
 
## -remarks

## -see-also

