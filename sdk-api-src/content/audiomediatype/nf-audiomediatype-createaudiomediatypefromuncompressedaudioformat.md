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

# CreateAudioMediaTypeFromUncompressedAudioFormat function


## -description


The <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function uses the information provided in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff538640">UNCOMPRESSEDAUDIOFORMAT</a> structure to create a media type object that describes the audio format.


## -parameters




### -param pUncompressedAudioFormat

Specifies a pointer to an UNCOMPRESSEDAUDIOFORMAT structure.


### -param ppIAudioMediaType

Specifies a pointer to an <a href="https://msdn.microsoft.com/library/windows/hardware/ff536496">IAudioMediaType</a> interface.


## -returns



The <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function returns S_OK if the call to the function is successful. Otherwise, it returns an appropriate HRESULT error code.




## -remarks



When you implement custom audio system effects, the <code>CreateAudioMediaTypeFromUncompressedAudioFormat</code> function works with <a href="https://msdn.microsoft.com/library/windows/hardware/ff536516">IAudioSystemEffectsCustomFormats::GetFormat</a> to represent a custom audio data format and to provide information about the custom format.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff536496">IAudioMediaType</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff536516">IAudioSystemEffectsCustomFormats::GetFormat</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff538640">UNCOMPRESSEDAUDIOFORMAT</a>
 

 

