---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.Open
title: IRDPSRAPITransportStream::Open (rdpencomapi.h)
description: Called by the Remote Desktop Protocol (RDP) stack to start the stream and indicate that the RDP stack is ready to receive notifications of events.
helpviewer_keywords: ["IRDPSRAPITransportStream interface [RDP]","Open method","IRDPSRAPITransportStream.Open","IRDPSRAPITransportStream::Open","Open","Open method [RDP]","Open method [RDP]","IRDPSRAPITransportStream interface","rdp.irdpsrapitransportstream_open","rdpencomapi/IRDPSRAPITransportStream::Open"]
old-location: rdp\irdpsrapitransportstream_open.htm
tech.root: rdp
ms.assetid: 55d53ed6-8046-4605-b543-ab0e5ad8d8f7
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStream interface [RDP],Open method, IRDPSRAPITransportStream.Open, IRDPSRAPITransportStream::Open, Open, Open method [RDP], Open method [RDP],IRDPSRAPITransportStream interface, rdp.irdpsrapitransportstream_open, rdpencomapi/IRDPSRAPITransportStream::Open
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
 - IRDPSRAPITransportStream::Open
 - rdpencomapi/IRDPSRAPITransportStream::Open
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
 - IRDPSRAPITransportStream.Open
---

# IRDPSRAPITransportStream::Open


## -description

Called by the Remote Desktop Protocol (RDP) stack to start the stream and indicate that the RDP stack is ready to receive notifications of events.

## -parameters

### -param pCallbacks [in]

Type: <b><a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreamevents">IRDPSRAPITransportStreamEvents</a>*</b>

An <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreamevents">IRDPSRAPITransportStreamEvents</a> interface pointer that will receive the transport stream events.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreamevents">IRDPSRAPITransportStreamEvents</a>