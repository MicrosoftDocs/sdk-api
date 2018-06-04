---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IAudioMediaType interface


## -description


The <code>IAudioMediaType</code> interface exposes methods that allow an sAPO to get information that is used to negotiate with the audio engine for the appropriate audio data format. An sAPO also returns this interface in response to a call to <a href="https://msdn.microsoft.com/library/windows/hardware/ff536516">IAudioSystemEffectsCustomFormats::GetFormat</a>.

<code>IAudioMediaType</code> inherits from <b>IUnknown</b> and also supports the following methods:
<dl>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536497">IAudioMediaType::GetAudioFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536498">IAudioMediaType::GetUncompressedAudioFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536499">IAudioMediaType::IsCompressedFormat</a>


</dd>
<dd>

<a href="https://msdn.microsoft.com/library/windows/hardware/ff536500">IAudioMediaType::IsEqual</a>


</dd>
</dl>
