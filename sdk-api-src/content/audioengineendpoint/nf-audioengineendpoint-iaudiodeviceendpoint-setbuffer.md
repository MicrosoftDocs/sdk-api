---
UID: NF:audioengineendpoint.IAudioDeviceEndpoint.SetBuffer
title: IAudioDeviceEndpoint::SetBuffer (audioengineendpoint.h)
description: Initializes the endpoint and creates a buffer based on the format of the endpoint into which the audio data is streamed.
helpviewer_keywords: ["IAudioDeviceEndpoint interface [Remote Desktop Services]","SetBuffer method","IAudioDeviceEndpoint.SetBuffer","IAudioDeviceEndpoint::SetBuffer","SetBuffer","SetBuffer method [Remote Desktop Services]","SetBuffer method [Remote Desktop Services]","IAudioDeviceEndpoint interface","audioengineendpoint/IAudioDeviceEndpoint::SetBuffer","termserv.iaudiodeviceendpoint_setbuffer"]
old-location: termserv\iaudiodeviceendpoint_setbuffer.htm
tech.root: TermServ
ms.assetid: 345a172b-11af-4c98-9f9c-54bfa38c5077
ms.date: 12/05/2018
ms.keywords: IAudioDeviceEndpoint interface [Remote Desktop Services],SetBuffer method, IAudioDeviceEndpoint.SetBuffer, IAudioDeviceEndpoint::SetBuffer, SetBuffer, SetBuffer method [Remote Desktop Services], SetBuffer method [Remote Desktop Services],IAudioDeviceEndpoint interface, audioengineendpoint/IAudioDeviceEndpoint::SetBuffer, termserv.iaudiodeviceendpoint_setbuffer
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
 - IAudioDeviceEndpoint::SetBuffer
 - audioengineendpoint/IAudioDeviceEndpoint::SetBuffer
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
 - IAudioDeviceEndpoint.SetBuffer
---

# IAudioDeviceEndpoint::SetBuffer


## -description

The <b>SetBuffer</b> method initializes the endpoint and creates a buffer based on the format of the endpoint into which the audio data is streamed.

## -parameters

### -param MaxPeriod [in]

The processing time, in 
    100-nanosecond units, of the audio endpoint.

### -param u32LatencyCoefficient [in]

The latency coefficient for the audio          device. This value is used to calculate the latency. Latency = <i>u32LatencyCoefficient</i> * <i>MaxPeriod</i>.

<div class="alert"><b>Note</b>  The device that the endpoint represents has a minimum latency
    value. If the value of this parameter is less than the minimum latency of the device or is zero, the
     endpoint object applies the minimum latency.  The audio engine can obtain the
    actual latency of the endpoint by calling the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-getlatency">IAudioEndpoint::GetLatency</a> method.</div>
<div> </div>

## -returns

If the method succeeds, it returns <b>S_OK</b>.

If it fails, possible return codes include, but are not limited to, the following.

## -remarks

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint">IAudioDeviceEndpoint</a>