---
UID: NF:audiomediatype.IAudioMediaType.IsCompressedFormat
title: IAudioMediaType::IsCompressedFormat
author: windows-sdk-content
description: The IsCompressedFormat method determines whether the audio data format is a compressed format.
old-location: audio\iaudiomediatype_iscompressedformat.htm
tech.root: audio
ms.assetid: db3ee751-7a7e-4e94-8dba-94065a7046f1
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: IAudioMediaType interface [Audio Devices],IsCompressedFormat method, IAudioMediaType.IsCompressedFormat, IAudioMediaType::IsCompressedFormat, IsCompressedFormat, IsCompressedFormat method [Audio Devices], IsCompressedFormat method [Audio Devices],IAudioMediaType interface, audio.iaudiomediatype_iscompressedformat, audio_syseffects_r_be58a0a1-340a-49bd-b47b-6f53ad5258ae.xml, audiomediatype/IAudioMediaType::IsCompressedFormat
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiomediatype.h
api_name:
 - IAudioMediaType.IsCompressedFormat
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- audiomediatype.h
: 
- IAudioMediaType.IsCompressedFormat
: 
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



