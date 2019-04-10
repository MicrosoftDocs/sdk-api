---
UID: NS:xaudio2.XAUDIO2_EFFECT_CHAIN
title: XAUDIO2_EFFECT_CHAIN (xaudio2.h)
author: windows-sdk-content
description: Defines an effect chain.
old-location: xaudio2\xaudio2_effect_chain.htm
tech.root: xaudio2
ms.assetid: T:Microsoft.directx_sdk.xaudio2.XAUDIO2_EFFECT_CHAIN
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: XAUDIO2_EFFECT_CHAIN, XAUDIO2_EFFECT_CHAIN structure [XAudio2 Audio Mixing APIs], xaudio2.xaudio2_effect_chain, xaudio2/XAUDIO2_EFFECT_CHAIN
ms.topic: struct
req.header: xaudio2.h
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
 - HeaderDef
api_location:
 - xaudio2.h
api_name:
 - XAUDIO2_EFFECT_CHAIN
product: Windows
targetos: Windows
req.typenames: XAUDIO2_EFFECT_CHAIN
req.redist: 
---

# XAUDIO2_EFFECT_CHAIN structure


## -description


Defines an effect chain.


## -struct-fields




### -field EffectCount

Number of effects in the effect chain for the voice.


### -field pEffectDescriptors

Array of <a href="https://msdn.microsoft.com/en-us/library/Ee419236(v=VS.85).aspx">XAUDIO2_EFFECT_DESCRIPTOR</a> structures containing pointers to XAPO instances.


## -remarks



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/4c33bd83-2654-cd6f-ea6c-bbc0d5872638">How to: Create an Effect Chain</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh405048(v=VS.85).aspx">IXAudio2::CreateMasteringVoice</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee418607(v=VS.85).aspx">IXAudio2::CreateSourceVoice</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee418608(v=VS.85).aspx">IXAudio2::CreateSubmixVoice</a>



<a href="https://msdn.microsoft.com/en-us/library/Ee418594(v=VS.85).aspx">IXAudio2Voice::SetEffectChain</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>



<a href="https://msdn.microsoft.com/3656aaf9-7a3a-2a5b-50f5-d279ce8a9e6c">XAudio2 Structures</a>
 

 

