---
UID: NF:rdpencomapi.IRDPSRAPIAudioStream.Initialize
title: IRDPSRAPIAudioStream::Initialize (rdpencomapi.h)
description: Initializes the audio stream.
helpviewer_keywords: ["IRDPSRAPIAudioStream interface [RDP]","Initialize method","IRDPSRAPIAudioStream.Initialize","IRDPSRAPIAudioStream::Initialize","Initialize","Initialize method [RDP]","Initialize method [RDP]","IRDPSRAPIAudioStream interface","rdp.irdpsrapiaudiostream_initialize","rdpencomapi/IRDPSRAPIAudioStream::Initialize"]
old-location: rdp\irdpsrapiaudiostream_initialize.htm
tech.root: rdp
ms.assetid: EF94E441-1331-4317-A104-05BDA6738C5A
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAudioStream interface [RDP],Initialize method, IRDPSRAPIAudioStream.Initialize, IRDPSRAPIAudioStream::Initialize, Initialize, Initialize method [RDP], Initialize method [RDP],IRDPSRAPIAudioStream interface, rdp.irdpsrapiaudiostream_initialize, rdpencomapi/IRDPSRAPIAudioStream::Initialize
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
 - IRDPSRAPIAudioStream::Initialize
 - rdpencomapi/IRDPSRAPIAudioStream::Initialize
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
 - IRDPSRAPIAudioStream.Initialize
---

# IRDPSRAPIAudioStream::Initialize


## -description

Initializes the audio stream.

## -parameters

### -param pnPeriodInHundredNsIntervals [out]

On return, indicates the stream period in 100 nanosecond intervals. The collaboration sharer calculates how frequently to call the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-getbuffer">GetBuffer</a> method from this value.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-getbuffer">GetBuffer</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiaudiostream">IRDPSRAPIAudioStream</a>



<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-start">Start</a>