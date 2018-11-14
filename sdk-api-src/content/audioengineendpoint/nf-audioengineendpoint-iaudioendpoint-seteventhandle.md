---
UID: NF:audioengineendpoint.IAudioEndpoint.SetEventHandle
title: IAudioEndpoint::SetEventHandle
author: windows-sdk-content
description: Sets the handle for the event that the endpoint uses to signal that it has completed processing of a buffer.
old-location: termserv\iaudioendpoint_seteventhandle.htm
tech.root: termserv
ms.assetid: 9f0f216a-d785-42e9-b07d-f1f2568b5833
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IAudioEndpoint interface [Remote Desktop Services],SetEventHandle method, IAudioEndpoint.SetEventHandle, IAudioEndpoint::SetEventHandle, SetEventHandle, SetEventHandle method [Remote Desktop Services], SetEventHandle method [Remote Desktop Services],IAudioEndpoint interface, audioengineendpoint/IAudioEndpoint::SetEventHandle, termserv.iaudioendpoint_seteventhandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: audioengineendpoint.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
 - Audioengineendpoint.h
api_name:
 - IAudioEndpoint.SetEventHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- audioengineendpoint.h
: 
- IAudioEndpoint.SetEventHandle
: 
---

# IAudioEndpoint::SetEventHandle


## -description


The <b>SetEventHandle</b> method sets the handle for the event that the endpoint uses to signal that it has completed processing of a buffer.


## -parameters




### -param eventHandle [in]

The event handle used to invoke a buffer completion
    callback.


## -returns



If the method succeeds, it returns <b>S_OK</b>. If it fails, possible return codes include, but are not limited to, the following.




## -remarks



The <b>SetEventHandle</b> method sets the audio engine event handle on the endpoint. In this implementation, the caller should receive an error response of <b>AEERR_NOT_INITIALIZED</b> if the audio endpoint is not initialized or the buffer is not set by the <a href="https://msdn.microsoft.com/345a172b-11af-4c98-9f9c-54bfa38c5077">SetBuffer</a> method.

To get event notifications, the audio engine will have  set the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag on the endpoint. To set this flag, the audio engine calls  the <a href="https://msdn.microsoft.com/f6713912-ba7e-4e3e-95d9-8318c40a7042">IAudioEndpoint::SetStreamFlags</a> method.

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/a1bb3fe4-6051-4b9c-8270-70375e700f01">IAudioEndpoint</a>
 

 

