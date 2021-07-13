---
UID: NF:rdpencomapi.IRDPSRAPIAudioStream.FreeBuffer
title: IRDPSRAPIAudioStream::FreeBuffer (rdpencomapi.h)
description: Releases the hold on the buffer after the GetBuffer method is called.
helpviewer_keywords: ["FreeBuffer","FreeBuffer method [RDP]","FreeBuffer method [RDP]","IRDPSRAPIAudioStream interface","IRDPSRAPIAudioStream interface [RDP]","FreeBuffer method","IRDPSRAPIAudioStream.FreeBuffer","IRDPSRAPIAudioStream::FreeBuffer","rdp.irdpsrapiaudiostream_freebuffer","rdpencomapi/IRDPSRAPIAudioStream::FreeBuffer"]
old-location: rdp\irdpsrapiaudiostream_freebuffer.htm
tech.root: rdp
ms.assetid: 03926ABF-D5D0-4D13-B081-0085EC698E9F
ms.date: 12/05/2018
ms.keywords: FreeBuffer, FreeBuffer method [RDP], FreeBuffer method [RDP],IRDPSRAPIAudioStream interface, IRDPSRAPIAudioStream interface [RDP],FreeBuffer method, IRDPSRAPIAudioStream.FreeBuffer, IRDPSRAPIAudioStream::FreeBuffer, rdp.irdpsrapiaudiostream_freebuffer, rdpencomapi/IRDPSRAPIAudioStream::FreeBuffer
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
 - IRDPSRAPIAudioStream::FreeBuffer
 - rdpencomapi/IRDPSRAPIAudioStream::FreeBuffer
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
 - IRDPSRAPIAudioStream.FreeBuffer
---

# IRDPSRAPIAudioStream::FreeBuffer


## -description

Releases the hold on the buffer after the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-getbuffer">GetBuffer</a> method is  called.



## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiaudiostream">IRDPSRAPIAudioStream</a>
