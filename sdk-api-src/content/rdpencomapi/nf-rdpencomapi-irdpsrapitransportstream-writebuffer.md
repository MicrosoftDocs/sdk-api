---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.WriteBuffer
title: IRDPSRAPITransportStream::WriteBuffer
author: windows-sdk-content
description: Called by the Remote Desktop Protocol (RDP) stack to write the contents of a stream buffer to the network.
old-location: rdp\irdpsrapitransportstream_writebuffer.htm
old-project: Rdp
ms.assetid: 9e78360d-9ea6-4a74-8a20-5546057c24b0
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: IRDPSRAPITransportStream interface [RDP],WriteBuffer method, IRDPSRAPITransportStream.WriteBuffer, IRDPSRAPITransportStream::WriteBuffer, WriteBuffer, WriteBuffer method [RDP], WriteBuffer method [RDP],IRDPSRAPITransportStream interface, rdp.irdpsrapitransportstream_writebuffer, rdpencomapi/IRDPSRAPITransportStream::WriteBuffer
ms.prod: windows
ms.technology: windows-sdk
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
-	IRDPSRAPITransportStream.WriteBuffer
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRDPSRAPITransportStream::WriteBuffer


## -description


Called by the Remote Desktop Protocol (RDP) stack to write the contents of a stream buffer to the network.


## -parameters




### -param pBuffer [in]

Type: <b><a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="https://msdn.microsoft.com/44087315-7a71-4557-89b3-bf8c66ed10a4">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the buffer to write.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/18ac00d5-f574-463f-a34a-40c2dc16d4d8">IRDPSRAPITransportStream</a>
 

 

