---
UID: NF:audiomediatype.CreateAudioMediaType
title: CreateAudioMediaType function (audiomediatype.h)
description: The CreateAudioMediaType function uses the format specified by the caller to create a media type object that describes the audio format.
helpviewer_keywords: ["CreateAudioMediaType","CreateAudioMediaType function [Audio Devices]","audio.createaudiomediatype","audio_syseffects_r_3b76e8f4-37c5-479e-91d7-6620c2e2b9db.xml","audiomediatype/CreateAudioMediaType"]
old-location: audio\createaudiomediatype.htm
tech.root: audio
ms.assetid: 02f7b1e6-338a-4bea-9a22-21496a045be6
ms.date: 12/05/2018
ms.keywords: CreateAudioMediaType, CreateAudioMediaType function [Audio Devices], audio.createaudiomediatype, audio_syseffects_r_3b76e8f4-37c5-479e-91d7-6620c2e2b9db.xml, audiomediatype/CreateAudioMediaType
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
 - CreateAudioMediaType
 - audiomediatype/CreateAudioMediaType
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
 - CreateAudioMediaType
---

# CreateAudioMediaType function


## -description

The <code>CreateAudioMediaType</code> function uses the format specified by the caller to create a media type object that describes the audio format.

## -parameters

### -param pAudioFormat

Specifies a pointer to a WAVEFORMATEX structure.

### -param cbAudioFormatSize

Specifies the size of the WAVEFORMATEX structure pointed to by the <i>pAudioFormat</i> parameter.

### -param ppIAudioMediaType

Specifies a pointer to an <a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a> interface.

## -returns

The <code>CreateAudioMediaType</code> function returns S_OK if the call to the function is successful. Otherwise, it returns an appropriate HRESULT error code.

## -remarks

When you implement custom audio system effects, the <code>CreateAudioMediaType</code> function works with <a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformat">IAudioSystemEffectsCustomFormats::GetFormat</a> to represent a custom audio data format and to provide information about the custom format.

## -see-also

<a href="/windows/desktop/api/audiomediatype/nn-audiomediatype-iaudiomediatype">IAudioMediaType</a>



<a href="/windows/desktop/api/audioenginebaseapo/nf-audioenginebaseapo-iaudiosystemeffectscustomformats-getformat">IAudioSystemEffectsCustomFormats::GetFormat</a>



<a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a>