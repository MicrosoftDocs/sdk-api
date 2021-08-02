---
UID: NF:audioengineendpoint.IAudioDeviceEndpoint.GetEventDrivenCapable
title: IAudioDeviceEndpoint::GetEventDrivenCapable (audioengineendpoint.h)
description: Indicates whether the device endpoint is event driven. The device endpoint controls the period of the audio engine by setting events that signal buffer availability.
helpviewer_keywords: ["GetEventDrivenCapable","GetEventDrivenCapable method [Remote Desktop Services]","GetEventDrivenCapable method [Remote Desktop Services]","IAudioDeviceEndpoint interface","IAudioDeviceEndpoint interface [Remote Desktop Services]","GetEventDrivenCapable method","IAudioDeviceEndpoint.GetEventDrivenCapable","IAudioDeviceEndpoint::GetEventDrivenCapable","audioengineendpoint/IAudioDeviceEndpoint::GetEventDrivenCapable","termserv.iaudiodeviceendpoint_geteventdrivencapable"]
old-location: termserv\iaudiodeviceendpoint_geteventdrivencapable.htm
tech.root: TermServ
ms.assetid: 56ed44ee-44dd-4a56-a4cc-2983d4802773
ms.date: 12/05/2018
ms.keywords: GetEventDrivenCapable, GetEventDrivenCapable method [Remote Desktop Services], GetEventDrivenCapable method [Remote Desktop Services],IAudioDeviceEndpoint interface, IAudioDeviceEndpoint interface [Remote Desktop Services],GetEventDrivenCapable method, IAudioDeviceEndpoint.GetEventDrivenCapable, IAudioDeviceEndpoint::GetEventDrivenCapable, audioengineendpoint/IAudioDeviceEndpoint::GetEventDrivenCapable, termserv.iaudiodeviceendpoint_geteventdrivencapable
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
 - IAudioDeviceEndpoint::GetEventDrivenCapable
 - audioengineendpoint/IAudioDeviceEndpoint::GetEventDrivenCapable
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
 - IAudioDeviceEndpoint.GetEventDrivenCapable
---

# IAudioDeviceEndpoint::GetEventDrivenCapable


## -description

The <b>GetEventDrivenCapable</b> method indicates whether the device endpoint is event driven. The device endpoint controls the period of the audio engine  by setting events that signal buffer availability.

## -parameters

### -param pbisEventCapable [out]

A value of <b>TRUE</b> indicates that the device endpoint is event driven. A value of <b>FALSE</b> indicates that it is not event driven. If the endpoint device is event driven, the audio engine can receive events from an audio device endpoint.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

Call the <b>GetEventDrivenCapable</b> method before calling the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudiodeviceendpoint-setbuffer">IAudioDeviceEndpoint::SetBuffer</a> method, which initializes the device endpoint and creates a buffer. This allows the device endpoint to set up the structures needed for driving events.

If the audio engine requires an event driven device endpoint, it will:

<ul>
<li>Create an event and set the event handle on the device endpoint by calling the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-seteventhandle">IAudioEndpoint::SetEventHandle</a> method.</li>
<li>Specify event driven mode by setting the <b>AUDCLNT_STREAMFLAGS_EVENTCALLBACK</b> flag on the device endpoint by calling the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-setstreamflags">IAudioEndpoint::SetStreamFlags</a> method.</li>
</ul>
The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint">IAudioDeviceEndpoint</a>
