---
UID: NF:audioengineendpoint.IAudioDeviceEndpoint.GetRTCaps
title: IAudioDeviceEndpoint::GetRTCaps (audioengineendpoint.h)
description: Queries whether the audio device is real-time (RT)-capable. This method is not used in Remote Desktop Services implementations of IAudioDeviceEndpoint.
helpviewer_keywords: ["GetRTCaps","GetRTCaps method [Remote Desktop Services]","GetRTCaps method [Remote Desktop Services]","IAudioDeviceEndpoint interface","IAudioDeviceEndpoint interface [Remote Desktop Services]","GetRTCaps method","IAudioDeviceEndpoint.GetRTCaps","IAudioDeviceEndpoint::GetRTCaps","audioengineendpoint/IAudioDeviceEndpoint::GetRTCaps","termserv.iaudiodeviceendpoint_getrtcaps"]
old-location: termserv\iaudiodeviceendpoint_getrtcaps.htm
tech.root: TermServ
ms.assetid: ba8aa8c2-8d62-477a-b5c0-338c989c57a6
ms.date: 12/05/2018
ms.keywords: GetRTCaps, GetRTCaps method [Remote Desktop Services], GetRTCaps method [Remote Desktop Services],IAudioDeviceEndpoint interface, IAudioDeviceEndpoint interface [Remote Desktop Services],GetRTCaps method, IAudioDeviceEndpoint.GetRTCaps, IAudioDeviceEndpoint::GetRTCaps, audioengineendpoint/IAudioDeviceEndpoint::GetRTCaps, termserv.iaudiodeviceendpoint_getrtcaps
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
 - IAudioDeviceEndpoint::GetRTCaps
 - audioengineendpoint/IAudioDeviceEndpoint::GetRTCaps
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
 - IAudioDeviceEndpoint.GetRTCaps
---

# IAudioDeviceEndpoint::GetRTCaps


## -description

The <b>GetRTCaps</b> method queries whether the audio device is real-time (RT)-capable. This method is  not used in Remote Desktop Services implementations of <a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint">IAudioDeviceEndpoint</a>.

## -parameters

### -param pbIsRTCapable [out]

Receives <b>TRUE</b> if the audio device is RT-capable, or <b>FALSE</b> otherwise. Remote Desktop Services implementations should always return <b>FALSE</b>.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint">IAudioDeviceEndpoint</a>