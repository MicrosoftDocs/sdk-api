---
UID: NF:xaudio2.IXAudio2.RegisterForCallbacks
title: IXAudio2::RegisterForCallbacks
author: windows-sdk-content
description: Adds an IXAudio2EngineCallback pointer to the XAudio2 engine callback list.
old-location: xaudio2\ixaudio2_interface_registerforcallbacks.htm
tech.root: xaudio2
ms.assetid: M:Microsoft.directx_sdk.ixaudio2.IXAudio2.RegisterForCallbacks(IXAudio2EngineCallback)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IXAudio2 interface [XAudio2 Audio Mixing APIs],RegisterForCallbacks method, IXAudio2.RegisterForCallbacks, IXAudio2::RegisterForCallbacks, RegisterForCallbacks, RegisterForCallbacks method [XAudio2 Audio Mixing APIs], RegisterForCallbacks method [XAudio2 Audio Mixing APIs],IXAudio2 interface, xaudio2.ixaudio2_interface_registerforcallbacks, xaudio2/IXAudio2::RegisterForCallbacks
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
 - IXAudio2.RegisterForCallbacks
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xaudio2.h
: 
- IXAudio2.RegisterForCallbacks
: 
---

# IXAudio2::RegisterForCallbacks


## -description


Adds an <a href="https://msdn.microsoft.com/en-us/library/Ee415910(v=VS.85).aspx">IXAudio2EngineCallback</a> pointer to the <a href="https://msdn.microsoft.com/en-us/library/Ee415908(v=VS.85).aspx">XAudio2</a> engine callback list.


## -parameters




### -param pCallback [in]


<a href="https://msdn.microsoft.com/en-us/library/Ee415910(v=VS.85).aspx">IXAudio2EngineCallback</a> pointer to add to the <a href="https://msdn.microsoft.com/en-us/library/Ee415908(v=VS.85).aspx">XAudio2</a> engine callback list.


## -returns



Returns S_OK if successful, an error code otherwise. See <a href="https://msdn.microsoft.com/42a1c21c-4b14-114a-d79e-15a61eb2139b">XAudio2 Error Codes</a> for descriptions of XAudio2 specific error codes.




## -remarks



This method can be called multiple times, allowing different components or layers of the same application to manage their own engine callback implementations separately.



It is invalid to call <b>RegisterForCallbacks</b> from within a callback (that is, <a href="https://msdn.microsoft.com/en-us/library/Ee415910(v=VS.85).aspx">IXAudio2EngineCallback</a> or <a href="https://msdn.microsoft.com/en-us/library/Ee415919(v=VS.85).aspx">IXAudio2VoiceCallback</a>). If <b>RegisterForCallbacks</b> is called within a callback, it returns XAUDIO2_E_INVALID_CALL.



<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Windows 8, Windows Phone 8 (XAudio 2.8); DirectX SDK (XAudio 2.7)




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Ee415908(v=VS.85).aspx">IXAudio2</a>



<a href="https://msdn.microsoft.com/4fbd4229-f7ac-33b3-b4b7-f09150a60598">XAudio2 Callbacks</a>
 

 

