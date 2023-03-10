---
UID: NN:audiomediatype.IAudioMediaType
title: IAudioMediaType (audiomediatype.h)
description: The IAudioMediaType interface exposes methods that allow an sAPO to get information that is used to negotiate with the audio engine for the appropriate audio data format.
helpviewer_keywords: ["IAudioMediaType","IAudioMediaType interface [Audio Devices]","IAudioMediaType interface [Audio Devices]","described","audio.iaudiomediatype","audio_syseffects_r_8b31a96c-76bb-4090-a0e3-e7e16fb98ddc.xml","audiomediatype/IAudioMediaType"]
old-location: audio\iaudiomediatype.htm
tech.root: audio
ms.assetid: bf3ee44b-79f3-441a-91f9-a340dc146d67
ms.date: 12/05/2018
ms.keywords: IAudioMediaType, IAudioMediaType interface [Audio Devices], IAudioMediaType interface [Audio Devices],described, audio.iaudiomediatype, audio_syseffects_r_8b31a96c-76bb-4090-a0e3-e7e16fb98ddc.xml, audiomediatype/IAudioMediaType
req.header: audiomediatype.h
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioMediaType
 - audiomediatype/IAudioMediaType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiomediatype.h
api_name:
 - IAudioMediaType
---

# IAudioMediaType interface


## -description

The <code>IAudioMediaType</code> interface exposes methods that allow an sAPO to get information that is used to negotiate with the audio engine for the appropriate audio data format. An sAPO also returns this interface in response to a call to <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformat">IAudioSystemEffectsCustomFormats::GetFormat</a>.

<code>IAudioMediaType</code> inherits from <b>IUnknown</b> and also supports the following methods:
<dl>
<dd>

<a href="/windows/desktop/api/audiomediatype/nf-audiomediatype-iaudiomediatype-getaudioformat">IAudioMediaType::GetAudioFormat</a>


</dd>
<dd>

<a href="/windows/desktop/api/audiomediatype/nf-audiomediatype-iaudiomediatype-getuncompressedaudioformat">IAudioMediaType::GetUncompressedAudioFormat</a>


</dd>
<dd>

<a href="/windows/desktop/api/audiomediatype/nf-audiomediatype-iaudiomediatype-iscompressedformat">IAudioMediaType::IsCompressedFormat</a>


</dd>
<dd>

<a href="/windows/desktop/api/audiomediatype/nf-audiomediatype-iaudiomediatype-isequal">IAudioMediaType::IsEqual</a>


</dd>
</dl>