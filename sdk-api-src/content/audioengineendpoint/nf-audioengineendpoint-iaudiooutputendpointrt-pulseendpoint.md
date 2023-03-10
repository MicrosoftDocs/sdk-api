---
UID: NF:audioengineendpoint.IAudioOutputEndpointRT.PulseEndpoint
title: IAudioOutputEndpointRT::PulseEndpoint (audioengineendpoint.h)
description: Is reserved. (IAudioOutputEndpointRT.PulseEndpoint)
helpviewer_keywords: ["IAudioOutputEndpointRT interface [Remote Desktop Services]","PulseEndpoint method","IAudioOutputEndpointRT.PulseEndpoint","IAudioOutputEndpointRT::PulseEndpoint","PulseEndpoint","PulseEndpoint method [Remote Desktop Services]","PulseEndpoint method [Remote Desktop Services]","IAudioOutputEndpointRT interface","audioengineendpoint/IAudioOutputEndpointRT::PulseEndpoint","termserv.iaudiooutputendpointrt_pulseendpoint"]
old-location: termserv\iaudiooutputendpointrt_pulseendpoint.htm
tech.root: TermServ
ms.assetid: 8ab117d6-5b13-4420-9cf2-865ff2011806
ms.date: 12/05/2018
ms.keywords: IAudioOutputEndpointRT interface [Remote Desktop Services],PulseEndpoint method, IAudioOutputEndpointRT.PulseEndpoint, IAudioOutputEndpointRT::PulseEndpoint, PulseEndpoint, PulseEndpoint method [Remote Desktop Services], PulseEndpoint method [Remote Desktop Services],IAudioOutputEndpointRT interface, audioengineendpoint/IAudioOutputEndpointRT::PulseEndpoint, termserv.iaudiooutputendpointrt_pulseendpoint
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
 - IAudioOutputEndpointRT::PulseEndpoint
 - audioengineendpoint/IAudioOutputEndpointRT::PulseEndpoint
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
 - IAudioOutputEndpointRT.PulseEndpoint
---

# IAudioOutputEndpointRT::PulseEndpoint


## -description

The <b>PulseEndpoint</b> method is  reserved.

This method is called by the audio engine at the end of a processing pass. The event handle is set by calling the <a href="/windows/desktop/api/audioengineendpoint/nf-audioengineendpoint-iaudioendpoint-seteventhandle">IAudioEndpoint::SetEventHandle</a> method.



## -remarks

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt">IAudioOutputEndpointRT</a>
