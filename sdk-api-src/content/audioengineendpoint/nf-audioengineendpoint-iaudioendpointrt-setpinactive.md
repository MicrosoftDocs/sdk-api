---
UID: NF:audioengineendpoint.IAudioEndpointRT.SetPinActive
title: IAudioEndpointRT::SetPinActive (audioengineendpoint.h)
description: Notifies the endpoint that it must change the state of the underlying streaming resources to an active state.
helpviewer_keywords: ["IAudioEndpointRT interface [Remote Desktop Services]","SetPinActive method","IAudioEndpointRT.SetPinActive","IAudioEndpointRT::SetPinActive","SetPinActive","SetPinActive method [Remote Desktop Services]","SetPinActive method [Remote Desktop Services]","IAudioEndpointRT interface","audioengineendpoint/IAudioEndpointRT::SetPinActive","termserv.iaudioendpointrt_setpinactive"]
old-location: termserv\iaudioendpointrt_setpinactive.htm
tech.root: TermServ
ms.assetid: 6c445b06-d576-4474-be8f-b984c43d3765
ms.date: 12/05/2018
ms.keywords: IAudioEndpointRT interface [Remote Desktop Services],SetPinActive method, IAudioEndpointRT.SetPinActive, IAudioEndpointRT::SetPinActive, SetPinActive, SetPinActive method [Remote Desktop Services], SetPinActive method [Remote Desktop Services],IAudioEndpointRT interface, audioengineendpoint/IAudioEndpointRT::SetPinActive, termserv.iaudioendpointrt_setpinactive
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
 - IAudioEndpointRT::SetPinActive
 - audioengineendpoint/IAudioEndpointRT::SetPinActive
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
 - IAudioEndpointRT.SetPinActive
---

# IAudioEndpointRT::SetPinActive


## -description

The <b>SetPinActive</b> method notifies the endpoint that it must change the state of the underlying streaming resources to an active state.



## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

This method enables the audio engine to call into the endpoint to indicate that the endpoint must prepare any audio stream resources. In most cases, this method can simply return <b>S_OK</b>.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt">IAudioEndpointRT</a>
