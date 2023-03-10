---
UID: NF:audioengineendpoint.IAudioEndpointRT.ProcessingComplete
title: IAudioEndpointRT::ProcessingComplete (audioengineendpoint.h)
description: Notifies the endpoint that a processing pass has been completed.
helpviewer_keywords: ["IAudioEndpointRT interface [Remote Desktop Services]","ProcessingComplete method","IAudioEndpointRT.ProcessingComplete","IAudioEndpointRT::ProcessingComplete","ProcessingComplete","ProcessingComplete method [Remote Desktop Services]","ProcessingComplete method [Remote Desktop Services]","IAudioEndpointRT interface","audioengineendpoint/IAudioEndpointRT::ProcessingComplete","termserv.iaudioendpointrt_processingcomplete"]
old-location: termserv\iaudioendpointrt_processingcomplete.htm
tech.root: TermServ
ms.assetid: 1a9c52fa-27ff-4e63-ae87-f5a3cd8d4f9b
ms.date: 12/05/2018
ms.keywords: IAudioEndpointRT interface [Remote Desktop Services],ProcessingComplete method, IAudioEndpointRT.ProcessingComplete, IAudioEndpointRT::ProcessingComplete, ProcessingComplete, ProcessingComplete method [Remote Desktop Services], ProcessingComplete method [Remote Desktop Services],IAudioEndpointRT interface, audioengineendpoint/IAudioEndpointRT::ProcessingComplete, termserv.iaudioendpointrt_processingcomplete
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
 - IAudioEndpointRT::ProcessingComplete
 - audioengineendpoint/IAudioEndpointRT::ProcessingComplete
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
 - IAudioEndpointRT.ProcessingComplete
---

# IAudioEndpointRT::ProcessingComplete


## -description

The <b>ProcessingComplete</b> method notifies the endpoint that a processing pass has been completed.



## -remarks

This method enables the audio engine to call into the endpoint to set an event that indicates
    that a processing pass had been completed and that there is audio data ready to be retrieved or passed to
    the endpoint device.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt">IAudioEndpointRT</a>
