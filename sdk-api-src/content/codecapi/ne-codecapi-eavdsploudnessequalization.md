---
UID: NE:codecapi.eAVDSPLoudnessEqualization
title: eAVDSPLoudnessEqualization
author: windows-sdk-content
description: Specifies whether loudness equalization is enabled in an audio decoder or digital signal processor (DSP).
old-location: dshow\eavdsploudnessequalization.htm
old-project: DirectShow
ms.assetid: bb46653e-d17d-4899-8a0b-cee8c4d68993
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: codecapi/eAVDSPLoudnessEqualization, codecapi/eAVDSPLoudnessEqualization_AUTO, codecapi/eAVDSPLoudnessEqualization_OFF, codecapi/eAVDSPLoudnessEqualization_ON, dshow.eavdsploudnessequalization, eAVDSPLoudnessEqualization, eAVDSPLoudnessEqualization enumeration [DirectShow], eAVDSPLoudnessEqualization_AUTO, eAVDSPLoudnessEqualization_OFF, eAVDSPLoudnessEqualization_ON
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
 - eAVDSPLoudnessEqualization
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# eAVDSPLoudnessEqualization enumeration


## -description


Specifies whether loudness equalization is enabled in an audio decoder or digital signal processor (DSP). This enumeration is used with the <a href="https://msdn.microsoft.com/f02b187f-1bcb-47b3-8ac2-018ed30491c6">AVDSPLoudnessEqualization</a> property.


## -enum-fields




### -field eAVDSPLoudnessEqualization_OFF

Loudness equalization is disabled.


### -field eAVDSPLoudnessEqualization_ON

Loudness equalization is enabled.


### -field eAVDSPLoudnessEqualization_AUTO

The decoder or DSP automatically selects the equalization mode.


## -remarks



Loudness equalization is a DSP process that maintains a consistent volume level when the audio stream changes.




## -see-also




<a href="https://msdn.microsoft.com/5d6e48cb-d181-448e-a96e-e5ab500427d7">Codec API Enumerations</a>



<a href="https://msdn.microsoft.com/cc3f1bd9-1d36-45e6-94e2-07f2800fd073">ICodecAPI Interface</a>
 

 

