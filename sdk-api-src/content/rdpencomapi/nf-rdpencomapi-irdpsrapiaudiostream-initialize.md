---
UID: NF:rdpencomapi.IRDPSRAPIAudioStream.Initialize
title: IRDPSRAPIAudioStream::Initialize
author: windows-sdk-content
description: Initializes the audio stream.
old-location: rdp\irdpsrapiaudiostream_initialize.htm
old-project: Rdp
ms.assetid: EF94E441-1331-4317-A104-05BDA6738C5A
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: IRDPSRAPIAudioStream interface [RDP],Initialize method, IRDPSRAPIAudioStream.Initialize, IRDPSRAPIAudioStream::Initialize, Initialize, Initialize method [RDP], Initialize method [RDP],IRDPSRAPIAudioStream interface, rdp.irdpsrapiaudiostream_initialize, rdpencomapi/IRDPSRAPIAudioStream::Initialize
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
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncom.dll
api_name:
-	IRDPSRAPIAudioStream.Initialize
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRDPSRAPIAudioStream::Initialize


## -description


Initializes the audio stream.


## -parameters




### -param pnPeriodInHundredNsIntervals [out]

On return, indicates the stream period in 100 nanosecond intervals. The collaboration sharer calculates how frequently to call the <a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a> method from this value.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/jj983413">GetBuffer</a>



<a href="https://msdn.microsoft.com/B2BC04A1-DE22-4543-9F10-33B0B99E0F92">IRDPSRAPIAudioStream</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/hh973223">Start</a>
 

 

