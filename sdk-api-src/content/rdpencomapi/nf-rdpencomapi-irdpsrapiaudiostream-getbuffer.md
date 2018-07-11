---
UID: NF:rdpencomapi.IRDPSRAPIAudioStream.GetBuffer
title: IRDPSRAPIAudioStream::GetBuffer
author: windows-sdk-content
description: Gets audio data from the buffer.
old-location: rdp\irdpsrapiaudiostream_getbuffer.htm
old-project: rdp
ms.assetid: 9A155107-1C43-49C2-BA92-4CBF37AEF4DB
ms.author: windowssdkdev
ms.date: 03/29/2018
ms.keywords: GetBuffer, GetBuffer method [RDP], GetBuffer method [RDP],IRDPSRAPIAudioStream interface, IRDPSRAPIAudioStream interface [RDP],GetBuffer method, IRDPSRAPIAudioStream.GetBuffer, IRDPSRAPIAudioStream::GetBuffer, rdp.irdpsrapiaudiostream_getbuffer, rdpencomapi/IRDPSRAPIAudioStream::GetBuffer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAudioStream.GetBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: ADAM
---

# IRDPSRAPIAudioStream::GetBuffer


## -description


Gets audio data from the buffer.   
   This method locks an internal buffer and returns a pointer to a specific location in that buffer. It does not  allocate a copy of the buffer for the caller.  To release the buffer after the last call to this method,   call  the <a href="https://msdn.microsoft.com/03926ABF-D5D0-4D13-B081-0085EC698E9F">FreeBuffer</a> method.


## -parameters




### -param ppbData [out]

A pointer to the current location in the buffer.


### -param pcbData [out]

The size in bytes of the available data in the buffer.


### -param pTimestamp [out]

The time-based location of the location pointer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/03926ABF-D5D0-4D13-B081-0085EC698E9F">FreeBuffer</a>



<a href="https://msdn.microsoft.com/B2BC04A1-DE22-4543-9F10-33B0B99E0F92">IRDPSRAPIAudioStream</a>
 

 

