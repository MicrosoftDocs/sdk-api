---
UID: NF:xaudio2.IXAudio2EngineCallback.OnCriticalError
title: IXAudio2EngineCallback::OnCriticalError
author: windows-sdk-content
description: Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.
old-location: xaudio2\ixaudio2enginecallback_oncriticalerror.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2enginecallback.IXAudio2EngineCallback.OnCriticalError(HRESULT)
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IXAudio2EngineCallback interface [XAudio2 Audio Mixing APIs],OnCriticalError method, IXAudio2EngineCallback.OnCriticalError, IXAudio2EngineCallback::OnCriticalError, OnCriticalError, OnCriticalError method [XAudio2 Audio Mixing APIs], OnCriticalError method [XAudio2 Audio Mixing APIs],IXAudio2EngineCallback interface, xaudio2.ixaudio2enginecallback_oncriticalerror, xaudio2/IXAudio2EngineCallback::OnCriticalError
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xaudio2.h
api_name:
 - IXAudio2EngineCallback.OnCriticalError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IXAudio2EngineCallback::OnCriticalError


## -description


Called if a critical system error occurs that requires XAudio2 to be closed down and restarted.


## -parameters




### -param Error

Error code returned by XAudio2.


## -returns



This method does not return a value.




## -remarks



If you provide the ID of a  specific device in the <i>szDeviceId</i> parameter to   <a href="https://msdn.microsoft.com/2E8163C6-60E9-4EA9-AD5A-A7F3C84FF6CF">IXAudio2::CreateMasteringVoice</a> or use the XAUDIO2_NO_VIRTUAL_AUDIO_CLIENT flag, then a critical error will occur and <b>OnCriticalError</b> is raised if the underlying WASAPI rendering device becomes unavailable. This can occur when a headset or speaker is unplugged or when a USB audio device is removed, for example.   Once a critical error has occurred, audio processing stops and all further calls to XAudio2 fail. The only way to recover in this situation is to release the XAudio2 instance and create a new one.





If you specified NULL or  <i>szDeviceId</i> parameter to   <a href="https://msdn.microsoft.com/2E8163C6-60E9-4EA9-AD5A-A7F3C84FF6CF">IXAudio2::CreateMasteringVoice</a>, then the system uses a Virtual Audio Client to represent the audio endpoint. In this case, if the underlying WASAPI rendering device becomes unavailable, the system automatically selects a new audio rendering device for rendering, audio processing continues, and <b>OnCriticalError</b> is not raised.

On the mobile device family, a Virtual Audio Client is always used and <b>OnCriticalError</b> is never raised, regardless of the values you provide to    <a href="https://msdn.microsoft.com/2E8163C6-60E9-4EA9-AD5A-A7F3C84FF6CF">CreateMasteringVoice</a>.

For information about the <a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a> interface methods, see the <a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a> section.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 10 (XAudio2.9); Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/D71C117F-826F-41E9-98F4-C6024B3C5103">IXAudio2EngineCallback</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>
 

 

