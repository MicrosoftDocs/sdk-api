---
UID: NF:audioengineendpoint.IAudioEndpoint.SetStreamFlags
title: IAudioEndpoint::SetStreamFlags method
author: windows-driver-content
description: Sets the stream configuration flags on the audio endpoint.
old-location: termserv\iaudioendpoint_setstreamflags.htm
old-project: TermServ
ms.assetid: f6713912-ba7e-4e3e-95d9-8318c40a7042
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: IAudioEndpoint, IAudioEndpoint interface [Remote Desktop Services], SetStreamFlags method, IAudioEndpoint::SetStreamFlags, SetStreamFlags method [Remote Desktop Services], SetStreamFlags method [Remote Desktop Services], IAudioEndpoint interface, SetStreamFlags,IAudioEndpoint.SetStreamFlags, audioengineendpoint/IAudioEndpoint::SetStreamFlags, termserv.iaudioendpoint_setstreamflags
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
-	IAudioEndpoint.SetStreamFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAudioEndpoint::SetStreamFlags method


## -description



        The <b>SetStreamFlags</b> method sets the stream configuration flags on the audio endpoint.


## -parameters




### -param streamFlags [in]

A bitwise <b>OR</b> of one or more of the AUDCLNT_STREAMFLAGS_XXX constants.


## -returns



If the method succeeds, it returns <b>S_OK</b>.




## -remarks



This method must not be called from a real-time processing thread.

The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.




## -see-also




<a href="https://msdn.microsoft.com/a1bb3fe4-6051-4b9c-8270-70375e700f01">IAudioEndpoint</a>
 

 

