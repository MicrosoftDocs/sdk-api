---
UID: NF:xaudio2.IXAudio2SourceVoice.Start
title: IXAudio2SourceVoice::Start
author: windows-driver-content
description: Starts consumption and processing of audio by the voice. Delivers the result to any connected submix or mastering voices, or to the output device.
old-location: xaudio2\ixaudio2sourcevoice_interface_start.htm
old-project: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2sourcevoice.IXAudio2SourceVoice.Start(UINT32,UINT32)
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IXAudio2SourceVoice interface [XAudio2 Audio Mixing APIs],Start method, IXAudio2SourceVoice.Start, IXAudio2SourceVoice::Start, Start, Start method [XAudio2 Audio Mixing APIs], Start method [XAudio2 Audio Mixing APIs],IXAudio2SourceVoice interface, xaudio2.ixaudio2sourcevoice_interface_start, xaudio2/IXAudio2SourceVoice::Start
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
-	IXAudio2SourceVoice.Start
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Use Windows Update or a Windows Update Services Server to retrieve the update on Windows XP.
---

# IXAudio2SourceVoice::Start


## -description


Starts consumption and processing of audio by the voice. Delivers the result to any connected submix or mastering voices, or to the output device.


## -parameters




### -param X2DEFAULT






#### - Flags [in]

Flags that control how the voice is started. Must be 0.


#### - OperationSet [in]


Identifies this call as part of a deferred batch. See the <a href="https://msdn.microsoft.com/5bfd747d-af65-f619-e549-be8130748261">XAudio2 Operation Sets</a> overview for more information.


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.




## -remarks



If the XAudio2 engine is stopped, the voice stops running. However, it remains in the started state, so that it starts running again as soon as the engine starts.



When first created, source voices are in the stopped state. Submix and mastering voices are in the started state.



After <b>Start</b> is called it has no further effect if called again before <a href="https://msdn.microsoft.com/A46CF7D1-5BBD-45F2-9C2A-90FE51A6FA75">IXAudio2SourceVoice::Stop</a> is called. In addition multiple calls to <b>Start</b> without matching calls to <b>IXAudio2SourceVoice::Stop</b> will result in warning messages in debug builds.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/40f79959-23c9-4513-363b-2f2fc85e4c0a">How to: Build a Basic Audio Processing Graph</a>



<a href="https://msdn.microsoft.com/48b80a66-91c1-973f-069b-6f63422d7154">How to: Stream a Sound from Disk</a>



<a href="https://msdn.microsoft.com/116DD0E0-8F0B-4934-A48D-FDBE0D0DF049">IXAudio2SourceVoice</a>



<a href="https://msdn.microsoft.com/F704008E-AE43-4189-8B34-8E3915338627">IXAudio2Voice</a>



<a href="https://msdn.microsoft.com/4fe88a0f-0234-462f-b575-e592f2c8401e">XAPO Overview</a>
 

 

