---
UID: NF:audioengineendpoint.IAudioEndpointControl.Start
title: IAudioEndpointControl::Start
author: windows-sdk-content
description: Starts the endpoint stream.
old-location: termserv\iaudioendpointcontrol_start.htm
tech.root: TermServ
ms.assetid: d9b54618-9750-49be-a966-1a2f02c81af6
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IAudioEndpointControl interface [Remote Desktop Services],Start method, IAudioEndpointControl.Start, IAudioEndpointControl::Start, Start, Start method [Remote Desktop Services], Start method [Remote Desktop Services],IAudioEndpointControl interface, audioengineendpoint/IAudioEndpointControl::Start, termserv.iaudioendpointcontrol_start
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
 - IAudioEndpointControl.Start
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAudioEndpointControl::Start


## -description


The <b>Start</b> method starts the endpoint stream.


## -parameters






## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



The implementation of this method can differ depending on the type of device that the endpoint represents.

This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/4514521a-e9a9-4f39-ab7d-4ef7e514bd10">IAudioEndpointControl</a>
 

 

