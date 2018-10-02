---
UID: NF:audiomediatype.IAudioMediaType.GetAudioFormat
title: IAudioMediaType::GetAudioFormat
author: windows-sdk-content
description: The GetAudioFormat method returns the WAVEFORMATEX structure for the audio data format.
old-location: audio\iaudiomediatype_getaudioformat.htm
tech.root: audio
ms.assetid: 5e00e566-3209-435a-85ae-2c209f0e0eb3
ms.author: windowssdkdev
ms.date: 09/28/2018
ms.keywords: GetAudioFormat, GetAudioFormat method [Audio Devices], GetAudioFormat method [Audio Devices],IAudioMediaType interface, IAudioMediaType interface [Audio Devices],GetAudioFormat method, IAudioMediaType.GetAudioFormat, IAudioMediaType::GetAudioFormat, audio.iaudiomediatype_getaudioformat, audio_syseffects_r_9859bef7-75b8-45eb-acc2-90c5d7ef5ee1.xml, audiomediatype/IAudioMediaType::GetAudioFormat
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
---

# IAudioMediaType::GetAudioFormat


## -description


The <code>GetAudioFormat</code> method returns the <a href="https://msdn.microsoft.com/f2f050d6-afe2-4647-932b-1287f4538702">WAVEFORMATEX</a> structure for the audio data format.


## -parameters






#### - None


## -returns



The <code>GetAudioFormat</code> method returns a pointer to a <a href="https://msdn.microsoft.com/f2f050d6-afe2-4647-932b-1287f4538702">WAVEFORMATEX</a> structure.




## -remarks



The pointer that is returned is valid only while the <b>IAudioMediaType</b> interface is referenced.




## -see-also




<a href="https://msdn.microsoft.com/f114e8ef-4fb7-4fdd-9c83-d8e74c91190e">WAVEFORMATEX</a>
 

 

