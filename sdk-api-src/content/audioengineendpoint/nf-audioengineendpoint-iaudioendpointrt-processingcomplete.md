---
UID: NF:audioengineendpoint.IAudioEndpointRT.ProcessingComplete
title: IAudioEndpointRT::ProcessingComplete method
author: windows-driver-content
description: Notifies the endpoint that a processing pass has been completed.
old-location: termserv\iaudioendpointrt_processingcomplete.htm
old-project: TermServ
ms.assetid: 1a9c52fa-27ff-4e63-ae87-f5a3cd8d4f9b
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IAudioEndpointRT, IAudioEndpointRT interface [Remote Desktop Services], ProcessingComplete method, IAudioEndpointRT::ProcessingComplete, ProcessingComplete method [Remote Desktop Services], ProcessingComplete method [Remote Desktop Services], IAudioEndpointRT interface, ProcessingComplete,IAudioEndpointRT.ProcessingComplete, audioengineendpoint/IAudioEndpointRT::ProcessingComplete, termserv.iaudioendpointrt_processingcomplete
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
-	IAudioEndpointRT.ProcessingComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpointRT::ProcessingComplete method


## -description



        The <b>ProcessingComplete</b> method notifies the endpoint that a processing pass has been completed.


## -parameters






## -returns



This method does not return a value.




## -remarks



This method enables the audio engine to call into the endpoint to set an event that indicates
    that a processing pass had been completed and that there is audio data ready to be retrieved or passed to
    the endpoint device.

This method can be called from a real-time processing thread. The
    implementation of this method must not block, access
    paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/3fb05ce4-a3be-4c84-8e03-71213f453f74">IAudioEndpointRT</a>
 

 

