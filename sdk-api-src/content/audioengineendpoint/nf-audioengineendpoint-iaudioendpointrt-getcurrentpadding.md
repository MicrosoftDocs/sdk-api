---
UID: NF:audioengineendpoint.IAudioEndpointRT.GetCurrentPadding
title: IAudioEndpointRT::GetCurrentPadding (audioengineendpoint.h)
description: Gets the amount, in 100-nanosecond units, of data that is queued up in the endpoint.
helpviewer_keywords: ["GetCurrentPadding","GetCurrentPadding method [Remote Desktop Services]","GetCurrentPadding method [Remote Desktop Services]","IAudioEndpointRT interface","IAudioEndpointRT interface [Remote Desktop Services]","GetCurrentPadding method","IAudioEndpointRT.GetCurrentPadding","IAudioEndpointRT::GetCurrentPadding","audioengineendpoint/IAudioEndpointRT::GetCurrentPadding","termserv.iaudioendpointrt_getcurrentpadding"]
old-location: termserv\iaudioendpointrt_getcurrentpadding.htm
tech.root: TermServ
ms.assetid: f61497c8-35da-4fbf-af83-1f15d5fe94f7
ms.date: 12/05/2018
ms.keywords: GetCurrentPadding, GetCurrentPadding method [Remote Desktop Services], GetCurrentPadding method [Remote Desktop Services],IAudioEndpointRT interface, IAudioEndpointRT interface [Remote Desktop Services],GetCurrentPadding method, IAudioEndpointRT.GetCurrentPadding, IAudioEndpointRT::GetCurrentPadding, audioengineendpoint/IAudioEndpointRT::GetCurrentPadding, termserv.iaudioendpointrt_getcurrentpadding
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
 - IAudioEndpointRT::GetCurrentPadding
 - audioengineendpoint/IAudioEndpointRT::GetCurrentPadding
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
 - IAudioEndpointRT.GetCurrentPadding
---

# IAudioEndpointRT::GetCurrentPadding


## -description

The <b>GetCurrentPadding</b> method gets the amount, in 100-nanosecond units, of data that is queued up in the endpoint.

## -parameters

### -param pPadding [out]

Receives the number of frames available in the endpoint buffer.

### -param pAeCurrentPosition [out]

Receives information about the position of the  current frame in the endpoint buffer in an <a href="/windows/desktop/api/audioengineendpoint/ns-audioengineendpoint-ae_current_position">AE_CURRENT_POSITION</a> structure specified by the caller.

## -remarks

The audio engine uses this information to calculate the amount of data that requires processing.
    This calculation depends on the implementation.
    The  value of the <i>pPadding</i> parameter specifies the number of audio frames that are queued up to play in the endpoint buffer. Before writing to the endpoint buffer, the audio engine can calculate the amount of available space in the buffer by subtracting the padding value from the buffer length. For a CaptureStream endpoint, the padding value reported by the <b>GetCurrentPadding</b> method specifies the number of frames of capture data that are available in the next packet in the endpoint buffer and that might be ready for the audio engine to read from the buffer.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt">IAudioEndpointRT</a>