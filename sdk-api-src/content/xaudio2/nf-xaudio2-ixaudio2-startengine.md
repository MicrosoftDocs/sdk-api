---
UID: NF:xaudio2.IXAudio2.StartEngine
title: IXAudio2::StartEngine method
author: windows-driver-content
description: Starts the audio processing thread.
old-location: xaudio2\ixaudio2_interface_startengine.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.StartEngine
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IXAudio2, IXAudio2 interface [XAudio2 Audio Mixing APIs], StartEngine method, IXAudio2::StartEngine, StartEngine method [XAudio2 Audio Mixing APIs], StartEngine method [XAudio2 Audio Mixing APIs], IXAudio2 interface, StartEngine,IXAudio2.StartEngine, xaudio2.ixaudio2_interface_startengine, xaudio2/IXAudio2::StartEngine
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: XAUDIO2_FILTER_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	xaudio2.h
api_name:
-	IXAudio2.StartEngine
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2::StartEngine method


## -description


Starts the audio processing thread.


## -parameters






## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.






## -remarks



After <b>StartEngine</b> is called, all started voices begin to consume audio. All enabled effects start running, and the resulting audio is sent to any connected output devices. When XAudio2 is first initialized, the engine is already in the started state.



It is invalid to call <b>StartEngine</b> from within a callback (that is, <a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a> or <a href="https://msdn.microsoft.com/FF78727D-16AE-40CB-BDE0-664687914FC0">IXAudio2VoiceCallback</a>). If <b>StartEngine</b> is called within a callback, it returns XAUDIO2_E_INVALID_CALL.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/A49469C6-2C29-407C-8C57-65E3FC9463F1">IXAudio2</a>
 

 

