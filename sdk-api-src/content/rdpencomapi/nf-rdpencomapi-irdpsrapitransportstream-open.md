---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.Open
title: IRDPSRAPITransportStream::Open (rdpencomapi.h)
author: windows-sdk-content
description: Called by the Remote Desktop Protocol (RDP) stack to start the stream and indicate that the RDP stack is ready to receive notifications of events.
old-location: rdp\irdpsrapitransportstream_open.htm
tech.root: rdp
ms.assetid: 55d53ed6-8046-4605-b543-ab0e5ad8d8f7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IRDPSRAPITransportStream interface [RDP],Open method, IRDPSRAPITransportStream.Open, IRDPSRAPITransportStream::Open, Open, Open method [RDP], Open method [RDP],IRDPSRAPITransportStream interface, rdp.irdpsrapitransportstream_open, rdpencomapi/IRDPSRAPITransportStream::Open
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
 - IRDPSRAPITransportStream.Open
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRDPSRAPITransportStream::Open


## -description


Called by the Remote Desktop Protocol (RDP) stack to start the stream and indicate that the RDP stack is ready to receive notifications of events.


## -parameters




### -param pCallbacks [in]

Type: <b><a href="https://msdn.microsoft.com/d38ee3fb-3867-40c9-8e6a-35c94762fdf4">IRDPSRAPITransportStreamEvents</a>*</b>

An <a href="https://msdn.microsoft.com/d38ee3fb-3867-40c9-8e6a-35c94762fdf4">IRDPSRAPITransportStreamEvents</a> interface pointer that will receive the transport stream events.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/18ac00d5-f574-463f-a34a-40c2dc16d4d8">IRDPSRAPITransportStream</a>



<a href="https://msdn.microsoft.com/d38ee3fb-3867-40c9-8e6a-35c94762fdf4">IRDPSRAPITransportStreamEvents</a>
 

 

