---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.FreeBuffer
title: IRDPSRAPITransportStream::FreeBuffer (rdpencomapi.h)
description: Called by the Remote Desktop Protocol (RDP) stack to return a stream buffer to the stream.
helpviewer_keywords: ["FreeBuffer","FreeBuffer method [RDP]","FreeBuffer method [RDP]","IRDPSRAPITransportStream interface","IRDPSRAPITransportStream interface [RDP]","FreeBuffer method","IRDPSRAPITransportStream.FreeBuffer","IRDPSRAPITransportStream::FreeBuffer","rdp.irdpsrapitransportstream_freebuffer","rdpencomapi/IRDPSRAPITransportStream::FreeBuffer"]
old-location: rdp\irdpsrapitransportstream_freebuffer.htm
tech.root: rdp
ms.assetid: db2f0bc2-cddf-44bd-9899-192e5eb014bb
ms.date: 12/05/2018
ms.keywords: FreeBuffer, FreeBuffer method [RDP], FreeBuffer method [RDP],IRDPSRAPITransportStream interface, IRDPSRAPITransportStream interface [RDP],FreeBuffer method, IRDPSRAPITransportStream.FreeBuffer, IRDPSRAPITransportStream::FreeBuffer, rdp.irdpsrapitransportstream_freebuffer, rdpencomapi/IRDPSRAPITransportStream::FreeBuffer
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
 - IRDPSRAPITransportStream::FreeBuffer
 - rdpencomapi/IRDPSRAPITransportStream::FreeBuffer
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
 - IRDPSRAPITransportStream.FreeBuffer
---

# IRDPSRAPITransportStream::FreeBuffer


## -description

Called by the Remote Desktop Protocol (RDP) stack to return a stream buffer to the stream.

## -parameters

### -param pBuffer [in]

Type: <b>IRDPSRAPITransportStreamBuffer*</b>

An <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the buffer to free.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a>