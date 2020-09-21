---
UID: NF:audiomediatype.IAudioMediaType.GetUncompressedAudioFormat
title: IAudioMediaType::GetUncompressedAudioFormat (audiomediatype.h)
description: The IAudioMediaType::GetUncompressedAudioFormat returns information about the audio data format.
helpviewer_keywords: ["GetUncompressedAudioFormat","GetUncompressedAudioFormat method [Audio Devices]","GetUncompressedAudioFormat method [Audio Devices]","IAudioMediaType interface","IAudioMediaType interface [Audio Devices]","GetUncompressedAudioFormat method","IAudioMediaType.GetUncompressedAudioFormat","IAudioMediaType::GetUncompressedAudioFormat","audio.iaudiomediatype_getuncompressedaudioformat","audio_syseffects_r_2e6e3723-2bc2-4e75-b64d-9b577d7916d6.xml","audiomediatype/IAudioMediaType::GetUncompressedAudioFormat"]
old-location: audio\iaudiomediatype_getuncompressedaudioformat.htm
tech.root: audio
ms.assetid: 9b4661cc-77b3-439b-bf28-5f9738dca6e1
ms.date: 12/05/2018
ms.keywords: GetUncompressedAudioFormat, GetUncompressedAudioFormat method [Audio Devices], GetUncompressedAudioFormat method [Audio Devices],IAudioMediaType interface, IAudioMediaType interface [Audio Devices],GetUncompressedAudioFormat method, IAudioMediaType.GetUncompressedAudioFormat, IAudioMediaType::GetUncompressedAudioFormat, audio.iaudiomediatype_getuncompressedaudioformat, audio_syseffects_r_2e6e3723-2bc2-4e75-b64d-9b577d7916d6.xml, audiomediatype/IAudioMediaType::GetUncompressedAudioFormat
req.header: audiomediatype.h
req.include-header: Audiomediatype.h
req.target-type: Desktop
req.target-min-winverclnt: Available in Windows Vista and later versions of Windows.
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
req.irql: All levels.
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioMediaType::GetUncompressedAudioFormat
 - audiomediatype/IAudioMediaType::GetUncompressedAudioFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiomediatype.h
api_name:
 - IAudioMediaType.GetUncompressedAudioFormat
---

# IAudioMediaType::GetUncompressedAudioFormat


## -description

The <code>IAudioMediaType::GetUncompressedAudioFormat</code> returns information about the audio data format.

## -parameters

### -param pUncompressedAudioFormat [out]

Specifies a pointer to an <a href="/windows/desktop/api/audiomediatype/ns-audiomediatype-uncompressedaudioformat">UNCOMPRESSEDAUDIOFORMAT</a> structure.

## -returns

The <code>GetUncompressedAudioFormat</code> method returns S_OK if it is successful. Otherwise, it returns an error code.

## -remarks

The information that is returned is useful for uncompressed formats. However, this method call will succeed for compressed formats as well. When you make this function call for a compressed audio data format, you must determine whether the returned information is applicable to your compressed format.

## -see-also

<a href="/windows/desktop/api/audiomediatype/ns-audiomediatype-uncompressedaudioformat">UNCOMPRESSEDAUDIOFORMAT</a>