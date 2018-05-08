---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.FreeBuffer
title: IRDPSRAPITransportStream::FreeBuffer
author: windows-driver-content
description: Called by the Remote Desktop Protocol (RDP) stack to return a stream buffer to the stream.
old-location: rdp\irdpsrapitransportstream_freebuffer.htm
old-project: Rdp
ms.assetid: db2f0bc2-cddf-44bd-9899-192e5eb014bb
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: FreeBuffer, FreeBuffer method [RDP], FreeBuffer method [RDP],IRDPSRAPITransportStream interface, IRDPSRAPITransportStream interface [RDP],FreeBuffer method, IRDPSRAPITransportStream.FreeBuffer, IRDPSRAPITransportStream::FreeBuffer, rdp.irdpsrapitransportstream_freebuffer, rdpencomapi/IRDPSRAPITransportStream::FreeBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
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
-	IRDPSRAPITransportStream.FreeBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IRDPSRAPITransportStream::FreeBuffer


## -description


Called by the Remote Desktop Protocol (RDP) stack to return a stream buffer to the stream.


## -parameters




### -param pBuffer [in]

Type: <b>IRDPSRAPITransportStreamBuffer*</b>

An <a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the buffer to free.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/18ac00d5-f574-463f-a34a-40c2dc16d4d8">IRDPSRAPITransportStream</a>
 

 

