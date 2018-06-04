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

# IXAudio2SourceVoice::GetFrequencyRatio


## -description


Returns the frequency adjustment ratio of the voice.


## -parameters




### -param pRatio [out]

Returns the current frequency adjustment ratio if successful.


## -returns



This method does not return a value.




## -remarks



<b>GetFrequencyRatio</b> always returns the voice's actual current frequency ratio. However, this may not match the ratio set by the most recent <a href="https://msdn.microsoft.com/58D458C3-528B-4696-8A24-2D66B93695C3">IXAudio2SourceVoice::SetFrequencyRatio</a> call: the actual ratio is only changed the next time the audio engine runs after the <b>IXAudio2SourceVoice::SetFrequencyRatio</b> call (or after the corresponding <a href="https://msdn.microsoft.com/2E798B7B-AD3E-4DCD-BB88-BAD3EC64EFE1">IXAudio2::CommitChanges</a> call, if <b>IXAudio2SourceVoice::SetFrequencyRatio</b> was called with a deferred operation ID).



For information on frequency ratios, see <a href="https://msdn.microsoft.com/58D458C3-528B-4696-8A24-2D66B93695C3">IXAudio2SourceVoice::SetFrequencyRatio</a>.


<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/116DD0E0-8F0B-4934-A48D-FDBE0D0DF049">IXAudio2SourceVoice</a>
 

 

