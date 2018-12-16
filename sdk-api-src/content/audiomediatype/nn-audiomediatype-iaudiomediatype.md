---
UID: NN:audiomediatype.IAudioMediaType
title: IAudioMediaType
author: windows-sdk-content
description: The IAudioMediaType interface exposes methods that allow an sAPO to get information that is used to negotiate with the audio engine for the appropriate audio data format.
old-location: audio\iaudiomediatype.htm
tech.root: audio
ms.assetid: bf3ee44b-79f3-441a-91f9-a340dc146d67
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioMediaType, IAudioMediaType interface [Audio Devices], IAudioMediaType interface [Audio Devices],described, audio.iaudiomediatype, audio_syseffects_r_8b31a96c-76bb-4090-a0e3-e7e16fb98ddc.xml, audiomediatype/IAudioMediaType
ms.topic: interface
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audiomediatype.h
api_name:
 - IAudioMediaType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioMediaType interface


## -description


The <code>IAudioMediaType</code> interface exposes methods that allow an sAPO to get information that is used to negotiate with the audio engine for the appropriate audio data format. An sAPO also returns this interface in response to a call to <a href="https://msdn.microsoft.com/0eab885f-32f7-47d3-b9b1-684eb3d2cd37">IAudioSystemEffectsCustomFormats::GetFormat</a>.

<code>IAudioMediaType</code> inherits from <b>IUnknown</b> and also supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/5e00e566-3209-435a-85ae-2c209f0e0eb3">IAudioMediaType::GetAudioFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/9b4661cc-77b3-439b-bf28-5f9738dca6e1">IAudioMediaType::GetUncompressedAudioFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/db3ee751-7a7e-4e94-8dba-94065a7046f1">IAudioMediaType::IsCompressedFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/a8ab9ad3-251d-43ab-b099-793ffc22b45f">IAudioMediaType::IsEqual</a>


</dd>
</dl>
