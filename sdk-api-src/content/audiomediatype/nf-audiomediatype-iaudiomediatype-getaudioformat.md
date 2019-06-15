---
UID: NF:audiomediatype.IAudioMediaType.GetAudioFormat
title: IAudioMediaType::GetAudioFormat (audiomediatype.h)
author: windows-sdk-content
description: The GetAudioFormat method returns the WAVEFORMATEX structure for the audio data format.
old-location: audio\iaudiomediatype_getaudioformat.htm
tech.root: audio
ms.assetid: 5e00e566-3209-435a-85ae-2c209f0e0eb3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetAudioFormat, GetAudioFormat method [Audio Devices], GetAudioFormat method [Audio Devices],IAudioMediaType interface, IAudioMediaType interface [Audio Devices],GetAudioFormat method, IAudioMediaType.GetAudioFormat, IAudioMediaType::GetAudioFormat, audio.iaudiomediatype_getaudioformat, audio_syseffects_r_9859bef7-75b8-45eb-acc2-90c5d7ef5ee1.xml, audiomediatype/IAudioMediaType::GetAudioFormat
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
req.lib: Audiomediatype.idl
req.dll: 
req.irql: All levels
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioMediaType::GetAudioFormat


## -description


The <code>GetAudioFormat</code> method returns the <a href="https://docs.microsoft.com/windows/desktop/api/mmreg/ns-mmreg-twaveformatex">WAVEFORMATEX</a> structure for the audio data format.


## -parameters






#### - None


## -returns



The <code>GetAudioFormat</code> method returns a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/mmreg/ns-mmreg-twaveformatex">WAVEFORMATEX</a> structure.




## -remarks



The pointer that is returned is valid only while the <b>IAudioMediaType</b> interface is referenced.




## -see-also




<a href="https://docs.microsoft.com/windows-hardware/drivers/ddi/content/ksmedia/ns-ksmedia-sysaudio_select_graph">WAVEFORMATEX</a>
 

 

