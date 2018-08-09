---
UID: NF:audiomediatype.IAudioMediaType.GetUncompressedAudioFormat
title: IAudioMediaType::GetUncompressedAudioFormat
author: windows-sdk-content
description: The IAudioMediaType::GetUncompressedAudioFormat returns information about the audio data format.
old-location: audio\iaudiomediatype_getuncompressedaudioformat.htm
old-project: audio
ms.assetid: 9b4661cc-77b3-439b-bf28-5f9738dca6e1
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetUncompressedAudioFormat, GetUncompressedAudioFormat method [Audio Devices], GetUncompressedAudioFormat method [Audio Devices],IAudioMediaType interface, IAudioMediaType interface [Audio Devices],GetUncompressedAudioFormat method, IAudioMediaType.GetUncompressedAudioFormat, IAudioMediaType::GetUncompressedAudioFormat, audio.iaudiomediatype_getuncompressedaudioformat, audio_syseffects_r_2e6e3723-2bc2-4e75-b64d-9b577d7916d6.xml, audiomediatype/IAudioMediaType::GetUncompressedAudioFormat
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AE_CURRENT_POSITION, *PAE_CURRENT_POSITION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - audiomediatype.h
api_name:
 - IAudioMediaType.GetUncompressedAudioFormat
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: All levels.
---

# IAudioMediaType::GetUncompressedAudioFormat


## -description


The <code>IAudioMediaType::GetUncompressedAudioFormat</code> returns information about the audio data format.


## -parameters




### -param pUncompressedAudioFormat [out]

Specifies a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff538640">UNCOMPRESSEDAUDIOFORMAT</a> structure.


## -returns



The <code>GetUncompressedAudioFormat</code> method returns S_OK if it is successful. Otherwise, it returns an error code.




## -remarks



The information that is returned is useful for uncompressed formats. However, this method call will succeed for compressed formats as well. When you make this function call for a compressed audio data format, you must determine whether the returned information is applicable to your compressed format.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538640">UNCOMPRESSEDAUDIOFORMAT</a>
 

 

