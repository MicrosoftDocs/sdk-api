---
UID: NE:codecapi.eAVDecAudioDualMono
title: eAVDecAudioDualMono
author: windows-sdk-content
description: Specifies whether the input audio stream is stereo or dual mono. This enumeration is used with the AVDecAudioDualMono property.
old-location: dshow\eavdecaudiodualmono.htm
old-project: DirectShow
ms.assetid: d9d3cc66-5622-4641-b302-6ecc6a05b1aa
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: codecapi/eAVDecAudioDualMono, codecapi/eAVDecAudioDualMono_IsDualMono, codecapi/eAVDecAudioDualMono_IsNotDualMono, codecapi/eAVDecAudioDualMono_UnSpecified, dshow.eavdecaudiodualmono, eAVDecAudioDualMono, eAVDecAudioDualMono enumeration [DirectShow], eAVDecAudioDualMonoEnumeration, eAVDecAudioDualMono_IsDualMono, eAVDecAudioDualMono_IsNotDualMono, eAVDecAudioDualMono_UnSpecified
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: codecapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - codecapi.h
api_name:
 - eAVDecAudioDualMono
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVDecAudioDualMono enumeration


## -description



Specifies whether the input audio stream is stereo or dual mono. This enumeration is used with the <a href="https://msdn.microsoft.com/en-us/library/Dd317616(v=VS.85).aspx">AVDecAudioDualMono</a> property.




## -enum-fields




### -field eAVDecAudioDualMono_IsNotDualMono

The input bit stream is not dual mono.


### -field eAVDecAudioDualMono_IsDualMono

The input bit stream is dual mono.


### -field eAVDecAudioDualMono_UnSpecified

There is no indication in the bit stream whether the audio is dual mono.


## -remarks



In dual mono encoding, each channel is encoded separately. In stereo encoding, both channels are encoded together.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd387884(v=VS.85).aspx">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd311953(v=VS.85).aspx">ICodecAPI Interface</a>
 

 

