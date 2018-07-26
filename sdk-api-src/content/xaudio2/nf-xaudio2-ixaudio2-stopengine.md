---
UID: NF:xaudio2.IXAudio2.StopEngine
title: IXAudio2::StopEngine
author: windows-sdk-content
description: Stops the audio processing thread.
old-location: xaudio2\ixaudio2_interface_stopengine.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.StopEngine
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],StopEngine method, IXAudio2.StopEngine, IXAudio2::StopEngine, StopEngine, StopEngine method [XAudio2 Audio Mixing APIs], StopEngine method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_stopengine, xaudio2/IXAudio2::StopEngine
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2.StopEngine
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2::StopEngine


## -description


Stops the audio processing thread.


## -parameters






## -returns



This method does not return a value.




## -remarks



When <b>StopEngine</b> is called, all output is stopped immediately. However, the audio graph is left untouched, preserving effect parameters, effect histories (for example, the data stored by a reverb effect in order to emit echoes of a previous sound), voice states, pending source buffers, cursor positions, and so forth. When the engine is restarted, the resulting audio output will be identical—apart from a period of silence—to the output that would have been produced if the engine had never been stopped.



It is invalid to call <b>StopEngine</b> from within a callback (that is, <a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a> or <a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a>).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); 
            Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>
 

 

