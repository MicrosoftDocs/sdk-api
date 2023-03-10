---
UID: NF:rdpencomapi.IRDPSRAPIAudioStream.GetBuffer
title: IRDPSRAPIAudioStream::GetBuffer (rdpencomapi.h)
description: Gets audio data from the buffer.
helpviewer_keywords: ["GetBuffer","GetBuffer method [RDP]","GetBuffer method [RDP]","IRDPSRAPIAudioStream interface","IRDPSRAPIAudioStream interface [RDP]","GetBuffer method","IRDPSRAPIAudioStream.GetBuffer","IRDPSRAPIAudioStream::GetBuffer","rdp.irdpsrapiaudiostream_getbuffer","rdpencomapi/IRDPSRAPIAudioStream::GetBuffer"]
old-location: rdp\irdpsrapiaudiostream_getbuffer.htm
tech.root: rdp
ms.assetid: 9A155107-1C43-49C2-BA92-4CBF37AEF4DB
ms.date: 12/05/2018
ms.keywords: GetBuffer, GetBuffer method [RDP], GetBuffer method [RDP],IRDPSRAPIAudioStream interface, IRDPSRAPIAudioStream interface [RDP],GetBuffer method, IRDPSRAPIAudioStream.GetBuffer, IRDPSRAPIAudioStream::GetBuffer, rdp.irdpsrapiaudiostream_getbuffer, rdpencomapi/IRDPSRAPIAudioStream::GetBuffer
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps \| UWP apps]
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
 - IRDPSRAPIAudioStream::GetBuffer
 - rdpencomapi/IRDPSRAPIAudioStream::GetBuffer
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
 - IRDPSRAPIAudioStream.GetBuffer
---

# IRDPSRAPIAudioStream::GetBuffer


## -description

Gets audio data from the buffer.   
   This method locks an internal buffer and returns a pointer to a specific location in that buffer. It does not  allocate a copy of the buffer for the caller.  To release the buffer after the last call to this method,   call  the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-freebuffer">FreeBuffer</a> method.

## -parameters

### -param ppbData [out]

A pointer to the current location in the buffer.

### -param pcbData [out]

The size in bytes of the available data in the buffer.

### -param pTimestamp [out]

The time-based location of the location pointer.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-freebuffer">FreeBuffer</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiaudiostream">IRDPSRAPIAudioStream</a>