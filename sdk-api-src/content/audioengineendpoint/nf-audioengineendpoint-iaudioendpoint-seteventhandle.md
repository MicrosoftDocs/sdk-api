---
UID: NF:audioengineendpoint.IAudioEndpoint.SetEventHandle
title: IAudioEndpoint::SetEventHandle (audioengineendpoint.h)
description: Sets the handle for the event that the endpoint uses to signal that it has completed processing of a buffer.
helpviewer_keywords: ["IAudioEndpoint interface [Remote Desktop Services]","SetEventHandle method","IAudioEndpoint.SetEventHandle","IAudioEndpoint::SetEventHandle","SetEventHandle","SetEventHandle method [Remote Desktop Services]","SetEventHandle method [Remote Desktop Services]","IAudioEndpoint interface","audioengineendpoint/IAudioEndpoint::SetEventHandle","termserv.iaudioendpoint_seteventhandle"]
old-location: termserv\iaudioendpoint_seteventhandle.htm
tech.root: TermServ
ms.assetid: 9f0f216a-d785-42e9-b07d-f1f2568b5833
ms.date: 12/05/2018
ms.keywords: IAudioEndpoint interface [Remote Desktop Services],SetEventHandle method, IAudioEndpoint.SetEventHandle, IAudioEndpoint::SetEventHandle, SetEventHandle, SetEventHandle method [Remote Desktop Services], SetEventHandle method [Remote Desktop Services],IAudioEndpoint interface, audioengineendpoint/IAudioEndpoint::SetEventHandle, termserv.iaudioendpoint_seteventhandle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAudioEndpoint::SetEventHandle
 - audioengineendpoint/IAudioEndpoint::SetEventHandle
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Audioengineendpoint.h
api_name:
 - IAudioEndpoint.SetEventHandle
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

The <b>SetEventHandle</b> method sets the audio engine event handle on the endpoint. In this implementation, the caller should receive an error response of <b>AEERR_NOT_INITIALIZED</b> if the audio endpoint is not initialized or the buffer is not set by the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiodeviceendpoint-setbuffer">SetBuffer</a> method.

To get event notifications, the audio engine will have  set the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag on the endpoint. To set this flag, the audio engine calls  the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-setstreamflags">IAudioEndpoint::SetStreamFlags</a> method.

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpoint">IAudioEndpoint</a>