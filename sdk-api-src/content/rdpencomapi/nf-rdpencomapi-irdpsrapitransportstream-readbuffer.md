---
UID: NF:rdpencomapi.IRDPSRAPITransportStream.ReadBuffer
title: IRDPSRAPITransportStream::ReadBuffer (rdpencomapi.h)
description: Called by the Remote Desktop Protocol (RDP) stack to read the contents of a stream buffer.
helpviewer_keywords: ["IRDPSRAPITransportStream interface [RDP]","ReadBuffer method","IRDPSRAPITransportStream.ReadBuffer","IRDPSRAPITransportStream::ReadBuffer","ReadBuffer","ReadBuffer method [RDP]","ReadBuffer method [RDP]","IRDPSRAPITransportStream interface","rdp.irdpsrapitransportstream_readbuffer","rdpencomapi/IRDPSRAPITransportStream::ReadBuffer"]
old-location: rdp\irdpsrapitransportstream_readbuffer.htm
tech.root: rdp
ms.assetid: 0a6d9a76-48b8-4755-985e-efbef01a6382
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStream interface [RDP],ReadBuffer method, IRDPSRAPITransportStream.ReadBuffer, IRDPSRAPITransportStream::ReadBuffer, ReadBuffer, ReadBuffer method [RDP], ReadBuffer method [RDP],IRDPSRAPITransportStream interface, rdp.irdpsrapitransportstream_readbuffer, rdpencomapi/IRDPSRAPITransportStream::ReadBuffer
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
 - IRDPSRAPITransportStream::ReadBuffer
 - rdpencomapi/IRDPSRAPITransportStream::ReadBuffer
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
 - IRDPSRAPITransportStream.ReadBuffer
---

# IRDPSRAPITransportStream::ReadBuffer


## -description

Called by the Remote Desktop Protocol (RDP) stack to read the contents of a stream buffer.

## -parameters

### -param pBuffer [in]

Type: <b><a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the buffer to read.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstream">IRDPSRAPITransportStream</a>