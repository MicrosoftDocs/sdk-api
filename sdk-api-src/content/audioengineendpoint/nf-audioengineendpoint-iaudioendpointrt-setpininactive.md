---
UID: NF:audioengineendpoint.IAudioEndpointRT.SetPinInactive
title: IAudioEndpointRT::SetPinInactive (audioengineendpoint.h)
author: windows-sdk-content
description: Notifies the endpoint that it must change the state of the underlying stream resources to an inactive state.
old-location: termserv\iaudioendpointrt_setpininactive.htm
tech.root: TermServ
ms.assetid: 07062063-cae1-4517-aeed-fb73ec602b27
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IAudioEndpointRT interface [Remote Desktop Services],SetPinInactive method, IAudioEndpointRT.SetPinInactive, IAudioEndpointRT::SetPinInactive, SetPinInactive, SetPinInactive method [Remote Desktop Services], SetPinInactive method [Remote Desktop Services],IAudioEndpointRT interface, audioengineendpoint/IAudioEndpointRT::SetPinInactive, termserv.iaudioendpointrt_setpininactive
ms.topic: method
f1_keywords: 
 - "audioengineendpoint/IAudioEndpointRT.SetPinInactive"
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
 - IAudioEndpointRT.SetPinInactive
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAudioEndpointRT::SetPinInactive


## -description


The <b>SetPinInactive</b> method     notifies the endpoint that it must change the state of the underlying stream resources to an inactive state.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



This method enables the audio engine to call into the endpoint to indicate that the endpoint can pause the underlying stream resources.  In most cases, this method can simply return <b>S_OK</b>.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt">IAudioEndpointRT</a>
 

 

