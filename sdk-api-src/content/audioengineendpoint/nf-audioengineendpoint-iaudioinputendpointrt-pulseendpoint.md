---
UID: NF:audioengineendpoint.IAudioInputEndpointRT.PulseEndpoint
title: IAudioInputEndpointRT::PulseEndpoint (audioengineendpoint.h)
description: Is reserved. (IAudioInputEndpointRT.PulseEndpoint)
helpviewer_keywords: ["IAudioInputEndpointRT interface [Remote Desktop Services]","PulseEndpoint method","IAudioInputEndpointRT.PulseEndpoint","IAudioInputEndpointRT::PulseEndpoint","PulseEndpoint","PulseEndpoint method [Remote Desktop Services]","PulseEndpoint method [Remote Desktop Services]","IAudioInputEndpointRT interface","audioengineendpoint/IAudioInputEndpointRT::PulseEndpoint","termserv.iaudioinputendpointrt_pulseendpoint"]
old-location: termserv\iaudioinputendpointrt_pulseendpoint.htm
tech.root: TermServ
ms.assetid: 2b23eac3-48e2-4d58-be6c-878967e7fa5c
ms.date: 12/05/2018
ms.keywords: IAudioInputEndpointRT interface [Remote Desktop Services],PulseEndpoint method, IAudioInputEndpointRT.PulseEndpoint, IAudioInputEndpointRT::PulseEndpoint, PulseEndpoint, PulseEndpoint method [Remote Desktop Services], PulseEndpoint method [Remote Desktop Services],IAudioInputEndpointRT interface, audioengineendpoint/IAudioInputEndpointRT::PulseEndpoint, termserv.iaudioinputendpointrt_pulseendpoint
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
 - IAudioInputEndpointRT::PulseEndpoint
 - audioengineendpoint/IAudioInputEndpointRT::PulseEndpoint
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
 - IAudioInputEndpointRT.PulseEndpoint
---

# IAudioInputEndpointRT::PulseEndpoint


## -description

The <b>PulseEndpoint</b> method  is reserved.



## -remarks

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt">IAudioInputEndpointRT</a>
