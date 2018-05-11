---
UID: NF:audioengineendpoint.IAudioEndpointRT.SetPinInactive
title: IAudioEndpointRT::SetPinInactive
author: windows-driver-content
description: Notifies the endpoint that it must change the state of the underlying stream resources to an inactive state.
old-location: termserv\iaudioendpointrt_setpininactive.htm
old-project: TermServ
ms.assetid: 07062063-cae1-4517-aeed-fb73ec602b27
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IAudioEndpointRT interface [Remote Desktop Services],SetPinInactive method, IAudioEndpointRT.SetPinInactive, IAudioEndpointRT::SetPinInactive, SetPinInactive, SetPinInactive method [Remote Desktop Services], SetPinInactive method [Remote Desktop Services],IAudioEndpointRT interface, audioengineendpoint/IAudioEndpointRT::SetPinInactive, termserv.iaudioendpointrt_setpininactive
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: AE_POSITION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Audioengineendpoint.h
api_name:
-	IAudioEndpointRT.SetPinInactive
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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




<a href="https://msdn.microsoft.com/3fb05ce4-a3be-4c84-8e03-71213f453f74">IAudioEndpointRT</a>
 

 

