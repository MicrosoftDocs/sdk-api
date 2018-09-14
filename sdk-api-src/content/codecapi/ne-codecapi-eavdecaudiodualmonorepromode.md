---
UID: NE:codecapi.eAVDecAudioDualMonoReproMode
title: eAVDecAudioDualMonoReproMode
author: windows-sdk-content
description: Specifies how the decoder reproduces dual mono audio. This enumeration is used with the AVDecAudioDualMonoReproMode property.
old-location: dshow\eavdecaudiodualmonorepromode.htm
tech.root: DirectShow
ms.assetid: 16374617-8342-4e8c-b52a-c5a419998699
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: codecapi/eAVDecAudioDualMonoReproMode, codecapi/eAVDecAudioDualMonoReproMode_LEFT_MONO, codecapi/eAVDecAudioDualMonoReproMode_MIX_MONO, codecapi/eAVDecAudioDualMonoReproMode_RIGHT_MONO, codecapi/eAVDecAudioDualMonoReproMode_STEREO, dshow.eavdecaudiodualmonorepromode, eAVDecAudioDualMonoReproMode, eAVDecAudioDualMonoReproMode enumeration [DirectShow], eAVDecAudioDualMonoReproModeEnumeration, eAVDecAudioDualMonoReproMode_LEFT_MONO, eAVDecAudioDualMonoReproMode_MIX_MONO, eAVDecAudioDualMonoReproMode_RIGHT_MONO, eAVDecAudioDualMonoReproMode_STEREO
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - codecapi.h
api_name:
 - eAVDecAudioDualMonoReproMode
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# eAVDecAudioDualMonoReproMode enumeration


## -description



Specifies how the decoder reproduces dual mono audio. This enumeration is used with the <a href="https://msdn.microsoft.com/3ef1f52c-13b2-4d9f-99fe-3317846be8a0">AVDecAudioDualMonoReproMode</a> property.




## -enum-fields




### -field eAVDecAudioDualMonoReproMode_STEREO

Output channel 1 (Ch1) to the left speaker and channel 2 (Ch2) to the right speaker.


### -field eAVDecAudioDualMonoReproMode_LEFT_MONO

Output Ch1 to the left and right speakers.


### -field eAVDecAudioDualMonoReproMode_RIGHT_MONO

Output Ch2 to the left and right speakers.


### -field eAVDecAudioDualMonoReproMode_MIX_MONO

Mix Ch1 and Ch2 and output the mix to the left and right speakers.


## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

