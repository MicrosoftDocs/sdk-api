---
UID: NF:audioengineendpoint.IAudioInputEndpointRT.PulseEndpoint
title: IAudioInputEndpointRT::PulseEndpoint method
author: windows-driver-content
description: Is reserved.
old-location: termserv\iaudioinputendpointrt_pulseendpoint.htm
old-project: TermServ
ms.assetid: 2b23eac3-48e2-4d58-be6c-878967e7fa5c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IAudioInputEndpointRT, IAudioInputEndpointRT interface [Remote Desktop Services], PulseEndpoint method, IAudioInputEndpointRT::PulseEndpoint, PulseEndpoint method [Remote Desktop Services], PulseEndpoint method [Remote Desktop Services], IAudioInputEndpointRT interface, PulseEndpoint,IAudioInputEndpointRT.PulseEndpoint, audioengineendpoint/IAudioInputEndpointRT::PulseEndpoint, termserv.iaudioinputendpointrt_pulseendpoint
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
-	IAudioInputEndpointRT.PulseEndpoint
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioInputEndpointRT::PulseEndpoint method


## -description



        The <b>PulseEndpoint</b> method  is reserved.


## -parameters






## -returns



This method does not return a value.




## -remarks



This method can be called from a real-time processing thread. The
    implementation of this method must not block, access paged memory, or call any blocking system routines.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/f9638dea-f61d-45f6-b91d-72e4fc1b4a92">IAudioInputEndpointRT</a>
 

 

