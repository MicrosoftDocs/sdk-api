---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.AllocBuffer
title: IRDPSRAPITransportStream::AllocBuffer (rdpencomapi.h)
description: Called by the Remote Desktop Protocol (RDP) stack to allocate a stream buffer.
helpviewer_keywords: ["AllocBuffer","AllocBuffer method [RDP]","AllocBuffer method [RDP]","IRDPSRAPITransportStream interface","IRDPSRAPITransportStream interface [RDP]","AllocBuffer method","IRDPSRAPITransportStream.AllocBuffer","IRDPSRAPITransportStream::AllocBuffer","rdp.irdpsrapitransportstream_allocbuffer","rdpencomapi/IRDPSRAPITransportStream::AllocBuffer"]
old-location: rdp\irdpsrapitransportstream_allocbuffer.htm
tech.root: rdp
ms.assetid: 5e53aedb-d3a2-4468-9df9-f058485d7bc4
ms.date: 12/05/2018
ms.keywords: AllocBuffer, AllocBuffer method [RDP], AllocBuffer method [RDP],IRDPSRAPITransportStream interface, IRDPSRAPITransportStream interface [RDP],AllocBuffer method, IRDPSRAPITransportStream.AllocBuffer, IRDPSRAPITransportStream::AllocBuffer, rdp.irdpsrapitransportstream_allocbuffer, rdpencomapi/IRDPSRAPITransportStream::AllocBuffer
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRDPSRAPITransportStream::AllocBuffer
 - rdpencomapi/IRDPSRAPITransportStream::AllocBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPITransportStream.AllocBuffer
---

# IRDPSRAPITransportStream::AllocBuffer


## -description

Called by the Remote Desktop Protocol (RDP) stack to allocate a stream buffer.

## -parameters

### -param maxPayload [in]

Type: <b>long</b>

The maximum size, in bytes, of the payload that will be placed into the buffer.

### -param ppBuffer [out, retval]

Type: <b><a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>**</b>

The address of an <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a> interface pointer that receives the buffer object.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>