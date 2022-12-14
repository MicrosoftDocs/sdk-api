---
UID: NF:audioengineendpoint.IAudioInputEndpointRT.ReleaseInputDataPointer
title: IAudioInputEndpointRT::ReleaseInputDataPointer (audioengineendpoint.h)
description: Releases the acquired data pointer.
helpviewer_keywords: ["IAudioInputEndpointRT interface [Remote Desktop Services]","ReleaseInputDataPointer method","IAudioInputEndpointRT.ReleaseInputDataPointer","IAudioInputEndpointRT::ReleaseInputDataPointer","ReleaseInputDataPointer","ReleaseInputDataPointer method [Remote Desktop Services]","ReleaseInputDataPointer method [Remote Desktop Services]","IAudioInputEndpointRT interface","audioengineendpoint/IAudioInputEndpointRT::ReleaseInputDataPointer","termserv.iaudioinputendpointrt_releaseinputdatapointer"]
old-location: termserv\iaudioinputendpointrt_releaseinputdatapointer.htm
tech.root: TermServ
ms.assetid: 9dd3f72a-79fe-4d07-a301-d0960e30a2d1
ms.date: 12/05/2018
ms.keywords: IAudioInputEndpointRT interface [Remote Desktop Services],ReleaseInputDataPointer method, IAudioInputEndpointRT.ReleaseInputDataPointer, IAudioInputEndpointRT::ReleaseInputDataPointer, ReleaseInputDataPointer, ReleaseInputDataPointer method [Remote Desktop Services], ReleaseInputDataPointer method [Remote Desktop Services],IAudioInputEndpointRT interface, audioengineendpoint/IAudioInputEndpointRT::ReleaseInputDataPointer, termserv.iaudioinputendpointrt_releaseinputdatapointer
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
 - IAudioInputEndpointRT::ReleaseInputDataPointer
 - audioengineendpoint/IAudioInputEndpointRT::ReleaseInputDataPointer
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
 - IAudioInputEndpointRT.ReleaseInputDataPointer
---

# IAudioInputEndpointRT::ReleaseInputDataPointer


## -description

The <b>ReleaseInputDataPointer</b> method releases the acquired data pointer.

## -parameters

### -param u32FrameCount [in]

The number of frames that have been
    consumed by the audio engine. This count might not
    be the same as the value returned by the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-getinputdatapointer">IAudioInputEndpointRT::GetInputDataPointer</a> method in the <i>pConnectionProperty</i>-&gt;<b>u32ValidFrameCount</b> member.

### -param pDataPointer [in]

The pointer to the buffer retrieved by                  the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioinputendpointrt-getinputdatapointer">GetInputDataPointer</a> method received  in the <i>pConnectionProperty</i>-&gt;<b>pBuffer</b> member.

## -remarks

<b>ReleaseInputDataPointer</b> notifies the endpoint that the audio engine no longer requires the input data pointer and also indicates the number of frames used during the session.
    For example, an endpoint, which represents a looped buffer, is connected to the input of the
    audio engine and can advance its read
    pointer by using the actual frame count.
    If <b>u32FrameCount</b> is zero, this indicates that the client did not use any data
    from the specified input buffer. The <b>u32FrameCount</b> must be less than or equal to the maximum  frame count supported by the endpoint. To get the supported number of frames, the audio engine calls the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-getframesperpacket">IAudioEndpoint::GetFramesPerPacket</a> method.

This method can be called from a real-time processing thread. The implementation of this method must not block, access paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt">IAudioInputEndpointRT</a>