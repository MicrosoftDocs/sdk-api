---
UID: NF:audioengineendpoint.IAudioEndpointControl.Reset
title: IAudioEndpointControl::Reset (audioengineendpoint.h)
description: Resets the endpoint stream.
helpviewer_keywords: ["IAudioEndpointControl interface [Remote Desktop Services]","Reset method","IAudioEndpointControl.Reset","IAudioEndpointControl::Reset","Reset","Reset method [Remote Desktop Services]","Reset method [Remote Desktop Services]","IAudioEndpointControl interface","audioengineendpoint/IAudioEndpointControl::Reset","termserv.iaudioendpointcontrol_reset"]
old-location: termserv\iaudioendpointcontrol_reset.htm
tech.root: TermServ
ms.assetid: f21a245c-b47b-425d-8054-330e265f16f1
ms.date: 12/05/2018
ms.keywords: IAudioEndpointControl interface [Remote Desktop Services],Reset method, IAudioEndpointControl.Reset, IAudioEndpointControl::Reset, Reset, Reset method [Remote Desktop Services], Reset method [Remote Desktop Services],IAudioEndpointControl interface, audioengineendpoint/IAudioEndpointControl::Reset, termserv.iaudioendpointcontrol_reset
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
 - IAudioEndpointControl::Reset
 - audioengineendpoint/IAudioEndpointControl::Reset
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
 - IAudioEndpointControl.Reset
---

# IAudioEndpointControl::Reset


## -description

The <b>Reset</b> method resets the endpoint stream.



## -returns

If the method succeeds, it returns <b>S_OK</b>.

## -remarks

<b>Reset</b> discards all data that has not been processed yet.
    The implementation of this method may differ depending on the type of device that the endpoint represents.

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.

## -see-also

<a href="/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol">IAudioEndpointControl</a>
