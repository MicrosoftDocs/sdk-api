---
UID: NF:audioengineendpoint.IAudioEndpoint.GetLatency
title: IAudioEndpoint::GetLatency (audioengineendpoint.h)
description: Gets the latency of the audio endpoint.
helpviewer_keywords: ["GetLatency","GetLatency method [Remote Desktop Services]","GetLatency method [Remote Desktop Services]","IAudioEndpoint interface","IAudioEndpoint interface [Remote Desktop Services]","GetLatency method","IAudioEndpoint.GetLatency","IAudioEndpoint::GetLatency","audioengineendpoint/IAudioEndpoint::GetLatency","termserv.iaudioendpoint_getlatency"]
old-location: termserv\iaudioendpoint_getlatency.htm
tech.root: TermServ
ms.assetid: 9afca6b7-2e0e-40a1-bb4a-932dad21b9eb
ms.date: 12/05/2018
ms.keywords: GetLatency, GetLatency method [Remote Desktop Services], GetLatency method [Remote Desktop Services],IAudioEndpoint interface, IAudioEndpoint interface [Remote Desktop Services],GetLatency method, IAudioEndpoint.GetLatency, IAudioEndpoint::GetLatency, audioengineendpoint/IAudioEndpoint::GetLatency, termserv.iaudioendpoint_getlatency
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
 - IAudioEndpoint::GetLatency
 - audioengineendpoint/IAudioEndpoint::GetLatency
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
 - IAudioEndpoint.GetLatency
---

# IAudioEndpoint::GetLatency


## -description

The <b>GetLatency</b> method gets the latency of the audio endpoint.

## -parameters

### -param pLatency [out]

A pointer to an <b>HNSTIME</b> variable that receives the latency that is added to the stream by the audio endpoint.

## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

There is some latency for an endpoint so that the buffer can stay ahead of the data already committed for input/output (I/O) transfer (playback or capture). For example, if an audio endpoint is using 5-millisecond buffers to stay ahead of the I/O transfer, the latency returned by this method is 5 milliseconds.

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpoint">IAudioEndpoint</a>