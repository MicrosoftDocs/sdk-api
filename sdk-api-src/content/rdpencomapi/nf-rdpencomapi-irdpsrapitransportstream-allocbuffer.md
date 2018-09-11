---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.AllocBuffer
title: IRDPSRAPITransportStream::AllocBuffer
author: windows-sdk-content
description: Called by the Remote Desktop Protocol (RDP) stack to allocate a stream buffer.
old-location: rdp\irdpsrapitransportstream_allocbuffer.htm
tech.root: Rdp
ms.assetid: 5e53aedb-d3a2-4468-9df9-f058485d7bc4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: AllocBuffer, AllocBuffer method [RDP], AllocBuffer method [RDP],IRDPSRAPITransportStream interface, IRDPSRAPITransportStream interface [RDP],AllocBuffer method, IRDPSRAPITransportStream.AllocBuffer, IRDPSRAPITransportStream::AllocBuffer, rdp.irdpsrapitransportstream_allocbuffer, rdpencomapi/IRDPSRAPITransportStream::AllocBuffer
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
 - IRDPSRAPITransportStream.AllocBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPITransportStream::AllocBuffer


## -description


Called by the Remote Desktop Protocol (RDP) stack to allocate a stream buffer.


## -parameters




### -param maxPayload [in]

Type: <b>long</b>

The maximum size, in bytes, of the payload that will be placed into the buffer.


### -param ppBuffer [out, retval]

Type: <b><a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>**</b>

The address of an <a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a> interface pointer that receives the buffer object.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/18ac00d5-f574-463f-a34a-40c2dc16d4d8">IRDPSRAPITransportStream</a>



<a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>
 

 

