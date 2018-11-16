---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.ReadBuffer
title: IRDPSRAPITransportStream::ReadBuffer
author: windows-sdk-content
description: Called by the Remote Desktop Protocol (RDP) stack to read the contents of a stream buffer.
old-location: rdp\irdpsrapitransportstream_readbuffer.htm
tech.root: Rdp
ms.assetid: 0a6d9a76-48b8-4755-985e-efbef01a6382
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRDPSRAPITransportStream interface [RDP],ReadBuffer method, IRDPSRAPITransportStream.ReadBuffer, IRDPSRAPITransportStream::ReadBuffer, ReadBuffer, ReadBuffer method [RDP], ReadBuffer method [RDP],IRDPSRAPITransportStream interface, rdp.irdpsrapitransportstream_readbuffer, rdpencomapi/IRDPSRAPITransportStream::ReadBuffer
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
 - IRDPSRAPITransportStream.ReadBuffer
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
- IRDPSRAPITransportStream.ReadBuffer
: 
---

# IRDPSRAPITransportStream::ReadBuffer


## -description


Called by the Remote Desktop Protocol (RDP) stack to read the contents of a stream buffer.


## -parameters




### -param pBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the buffer to read.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/18ac00d5-f574-463f-a34a-40c2dc16d4d8">IRDPSRAPITransportStream</a>
 

 

