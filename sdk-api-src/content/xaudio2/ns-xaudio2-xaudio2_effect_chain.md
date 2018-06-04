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

# XAUDIO2_EFFECT_CHAIN structure


## -description


Defines an effect chain.


## -struct-fields




### -field EffectCount

Number of effects in the effect chain for the voice.


### -field pEffectDescriptors

Array of <a href="https://msdn.microsoft.com/d2c7c640-9f6a-4fc0-bc87-35570281cec5">XAUDIO2_EFFECT_DESCRIPTOR</a> structures containing pointers to XAPO instances.


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/4c33bd83-2654-cd6f-ea6c-bbc0d5872638">How to: Create an Effect Chain</a>



<a href="https://msdn.microsoft.com/2E8163C6-60E9-4EA9-AD5A-A7F3C84FF6CF">IXAudio2::CreateMasteringVoice</a>



<a href="https://msdn.microsoft.com/5F37327B-A749-4D2D-A664-7DC45A13FF9A">IXAudio2::CreateSourceVoice</a>



<a href="https://msdn.microsoft.com/4073041D-19F8-44D7-BCCC-A9E0654B05D8">IXAudio2::CreateSubmixVoice</a>



<a href="https://msdn.microsoft.com/6CA630E6-66D5-495C-808D-79EE5E85D92B">IXAudio2Voice::SetEffectChain</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">XAudio2 Structures</a>
 

 

