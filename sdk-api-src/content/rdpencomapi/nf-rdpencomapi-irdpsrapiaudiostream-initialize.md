---
UID: NF:rdpencomapi.IRDPSRAPIAudioStream.Initialize
title: IRDPSRAPIAudioStream::Initialize
author: windows-sdk-content
description: Initializes the audio stream.
old-location: rdp\irdpsrapiaudiostream_initialize.htm
tech.root: Rdp
ms.assetid: EF94E441-1331-4317-A104-05BDA6738C5A
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IRDPSRAPIAudioStream interface [RDP],Initialize method, IRDPSRAPIAudioStream.Initialize, IRDPSRAPIAudioStream::Initialize, Initialize, Initialize method [RDP], Initialize method [RDP],IRDPSRAPIAudioStream interface, rdp.irdpsrapiaudiostream_initialize, rdpencomapi/IRDPSRAPIAudioStream::Initialize
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIAudioStream.Initialize
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rdpencomapi.h
: 
- IRDPSRAPIAudioStream.Initialize
: 
---

# IRDPSRAPIAudioStream::Initialize


## -description


Initializes the audio stream.


## -parameters




### -param pnPeriodInHundredNsIntervals [out]

On return, indicates the stream period in 100 nanosecond intervals. The collaboration sharer calculates how frequently to call the <a href="https://msdn.microsoft.com/9A155107-1C43-49C2-BA92-4CBF37AEF4DB">GetBuffer</a> method from this value.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/9A155107-1C43-49C2-BA92-4CBF37AEF4DB">GetBuffer</a>



<a href="https://msdn.microsoft.com/B2BC04A1-DE22-4543-9F10-33B0B99E0F92">IRDPSRAPIAudioStream</a>



<a href="https://msdn.microsoft.com/23ADA8F5-9F44-45E6-88DC-852D8F62F03F">Start</a>
 

 

