---
UID: NF:audioengineendpoint.IAudioEndpointControl.Stop
title: IAudioEndpointControl::Stop (audioengineendpoint.h)
description: Stops the endpoint stream.
old-location: termserv\iaudioendpointcontrol_stop.htm
tech.root: TermServ
ms.assetid: 803aec38-abc8-4f55-bb56-3dcc3eeb924a
ms.date: 12/05/2018
ms.keywords: IAudioEndpointControl interface [Remote Desktop Services],Stop method, IAudioEndpointControl.Stop, IAudioEndpointControl::Stop, Stop, Stop method [Remote Desktop Services], Stop method [Remote Desktop Services],IAudioEndpointControl interface, audioengineendpoint/IAudioEndpointControl::Stop, termserv.iaudioendpointcontrol_stop
ms.topic: method
f1_keywords:
- audioengineendpoint/IAudioEndpointControl.Stop
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Audioengineendpoint.h
api_name:
- IAudioEndpointControl.Stop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointControl::Stop


## -description


The <b>Stop</b> method stops the endpoint stream.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



The implementation of this method can differ depending on the type of device that the endpoint represents.

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol">IAudioEndpointControl</a>
 

 

