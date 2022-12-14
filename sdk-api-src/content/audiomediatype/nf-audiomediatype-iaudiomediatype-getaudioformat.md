---
UID: NF:audiomediatype.IAudioMediaType.GetAudioFormat
title: IAudioMediaType::GetAudioFormat (audiomediatype.h)
description: The GetAudioFormat method returns the WAVEFORMATEX structure for the audio data format.
helpviewer_keywords: ["GetAudioFormat","GetAudioFormat method [Audio Devices]","GetAudioFormat method [Audio Devices]","IAudioMediaType interface","IAudioMediaType interface [Audio Devices]","GetAudioFormat method","IAudioMediaType.GetAudioFormat","IAudioMediaType::GetAudioFormat","audio.iaudiomediatype_getaudioformat","audio_syseffects_r_9859bef7-75b8-45eb-acc2-90c5d7ef5ee1.xml","audiomediatype/IAudioMediaType::GetAudioFormat"]
old-location: audio\iaudiomediatype_getaudioformat.htm
tech.root: audio
ms.assetid: 5e00e566-3209-435a-85ae-2c209f0e0eb3
ms.date: 12/05/2018
ms.keywords: GetAudioFormat, GetAudioFormat method [Audio Devices], GetAudioFormat method [Audio Devices],IAudioMediaType interface, IAudioMediaType interface [Audio Devices],GetAudioFormat method, IAudioMediaType.GetAudioFormat, IAudioMediaType::GetAudioFormat, audio.iaudiomediatype_getaudioformat, audio_syseffects_r_9859bef7-75b8-45eb-acc2-90c5d7ef5ee1.xml, audiomediatype/IAudioMediaType::GetAudioFormat
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
req.lib: Audiomediatype.idl
req.dll: 
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioMediaType::GetAudioFormat
 - audiomediatype/IAudioMediaType::GetAudioFormat
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiomediatype.idl
 - Audiomediatype.idl.dll
api_name:
 - IAudioMediaType.GetAudioFormat
---

## -description

The <code>GetAudioFormat</code> method returns the <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> structure for the audio data format.



## -returns

The <code>GetAudioFormat</code> method returns a pointer to a <a href="/windows/win32/api/mmreg/ns-mmreg-waveformatex">WAVEFORMATEX</a> structure.

## -remarks

The pointer that is returned is valid only while the <b>IAudioMediaType</b> interface is referenced.

## -see-also

<a href="/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-sysaudio_select_graph">WAVEFORMATEX</a>
