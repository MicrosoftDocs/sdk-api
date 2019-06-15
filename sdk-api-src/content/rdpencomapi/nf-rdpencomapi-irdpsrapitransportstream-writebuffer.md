---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.WriteBuffer
title: IRDPSRAPITransportStream::WriteBuffer (rdpencomapi.h)
author: windows-sdk-content
description: Called by the Remote Desktop Protocol (RDP) stack to write the contents of a stream buffer to the network.
old-location: rdp\irdpsrapitransportstream_writebuffer.htm
tech.root: rdp
ms.assetid: 9e78360d-9ea6-4a74-8a20-5546057c24b0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStream interface [RDP],WriteBuffer method, IRDPSRAPITransportStream.WriteBuffer, IRDPSRAPITransportStream::WriteBuffer, WriteBuffer, WriteBuffer method [RDP], WriteBuffer method [RDP],IRDPSRAPITransportStream interface, rdp.irdpsrapitransportstream_writebuffer, rdpencomapi/IRDPSRAPITransportStream::WriteBuffer
ms.topic: method
f1_keywords: ["rdpencomapi/IRDPSRAPITransportStream.WriteBuffer"]
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
 - IRDPSRAPITransportStream.WriteBuffer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IRDPSRAPITransportStream::WriteBuffer


## -description


Called by the Remote Desktop Protocol (RDP) stack to write the contents of a stream buffer to the network.


## -parameters




### -param pBuffer [in]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the buffer to write.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a>
 

 

