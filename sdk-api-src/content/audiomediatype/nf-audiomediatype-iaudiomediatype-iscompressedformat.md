---
UID: NF:audiomediatype.IAudioMediaType.IsCompressedFormat
title: IAudioMediaType::IsCompressedFormat (audiomediatype.h)
description: The IsCompressedFormat method determines whether the audio data format is a compressed format.
helpviewer_keywords: ["IAudioMediaType interface [Audio Devices]","IsCompressedFormat method","IAudioMediaType.IsCompressedFormat","IAudioMediaType::IsCompressedFormat","IsCompressedFormat","IsCompressedFormat method [Audio Devices]","IsCompressedFormat method [Audio Devices]","IAudioMediaType interface","audio.iaudiomediatype_iscompressedformat","audio_syseffects_r_be58a0a1-340a-49bd-b47b-6f53ad5258ae.xml","audiomediatype/IAudioMediaType::IsCompressedFormat"]
old-location: audio\iaudiomediatype_iscompressedformat.htm
tech.root: audio
ms.assetid: db3ee751-7a7e-4e94-8dba-94065a7046f1
ms.date: 12/05/2018
ms.keywords: IAudioMediaType interface [Audio Devices],IsCompressedFormat method, IAudioMediaType.IsCompressedFormat, IAudioMediaType::IsCompressedFormat, IsCompressedFormat, IsCompressedFormat method [Audio Devices], IsCompressedFormat method [Audio Devices],IAudioMediaType interface, audio.iaudiomediatype_iscompressedformat, audio_syseffects_r_be58a0a1-340a-49bd-b47b-6f53ad5258ae.xml, audiomediatype/IAudioMediaType::IsCompressedFormat
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
req.irql: All levels
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioMediaType::IsCompressedFormat
 - audiomediatype/IAudioMediaType::IsCompressedFormat
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
 - IAudioMediaType.IsCompressedFormat
---

# IAudioMediaType::IsCompressedFormat


## -description

The <code>IsCompressedFormat</code> method determines whether the audio data format is a compressed format.

## -parameters

### -param pfCompressed [out]

Receives a Boolean value. The value is <b>TRUE</b> if the format is compressed or <b>FALSE</b> if the format is uncompressed.

## -returns

The <code>IsCompressedFormat</code> method returns S_OK if the audio data format is compressed, otherwise it returns an error code.

## -remarks

None.

