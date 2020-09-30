---
UID: NF:audiomediatype.CreateAudioMediaTypeFromUncompressedAudioFormat
title: CreateAudioMediaTypeFromUncompressedAudioFormat function (audiomediatype.h)
description: The CreateAudioMediaTypeFromUncompressedAudioFormat function uses the information provided in the UNCOMPRESSEDAUDIOFORMAT structure to create a media type object that describes the audio format.
helpviewer_keywords: ["CreateAudioMediaTypeFromUncompressedAudioFormat","CreateAudioMediaTypeFromUncompressedAudioFormat function [Audio Devices]","audio.createaudiomediatypefromuncompressedaudioformat","audio_syseffects_r_af85b8fb-5bdc-41f6-af2f-ee84ca999ac9.xml","audiomediatype/CreateAudioMediaTypeFromUncompressedAudioFormat"]
old-location: audio\createaudiomediatypefromuncompressedaudioformat.htm
tech.root: audio
ms.assetid: 48c9d15c-2e95-4a4a-b2cb-8a144569e45b
ms.date: 12/05/2018
ms.keywords: CreateAudioMediaTypeFromUncompressedAudioFormat, CreateAudioMediaTypeFromUncompressedAudioFormat function [Audio Devices], audio.createaudiomediatypefromuncompressedaudioformat, audio_syseffects_r_af85b8fb-5bdc-41f6-af2f-ee84ca999ac9.xml, audiomediatype/CreateAudioMediaTypeFromUncompressedAudioFormat
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
req.irql: N/A
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateAudioMediaTypeFromUncompressedAudioFormat
 - audiomediatype/CreateAudioMediaTypeFromUncompressedAudioFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - audiomediatype.h
api_name:
 - CreateAudioMediaTypeFromUncompressedAudioFormat
---

# CreateAudioMediaTypeFromUncompressedAudioFormat function


## -description

The <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function uses the information provided in the <a href="/windows/desktop/api/audiomediatype/ns-audiomediatype-uncompressedaudioformat">UNCOMPRESSEDAUDIOFORMAT</a> structure to create a media type object that describes the audio format.

## -parameters

### -param pUncompressedAudioFormat

Specifies a pointer to an UNCOMPRESSEDAUDIOFORMAT structure.

### -param ppIAudioMediaType

Specifies a pointer to an <a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a> interface.

## -returns

The <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function returns S_OK if the call to the function is successful. Otherwise, it returns an appropriate HRESULT error code.

## -remarks

When you implement custom audio system effects, the <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function works with <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformat">IAudioSystemEffectsCustomFormats::GetFormat</a> to represent a custom audio data format and to provide information about the custom format.

## -see-also

<a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a>



<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformat">IAudioSystemEffectsCustomFormats::GetFormat</a>



<a href="/windows/desktop/api/audiomediatype/ns-audiomediatype-uncompressedaudioformat">UNCOMPRESSEDAUDIOFORMAT</a>