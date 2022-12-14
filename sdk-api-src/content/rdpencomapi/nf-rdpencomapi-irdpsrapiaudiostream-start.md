---
UID: NF:rdpencomapi.IRDPSRAPIAudioStream.Start
title: IRDPSRAPIAudioStream::Start (rdpencomapi.h)
description: Starts the audio stream.
helpviewer_keywords: ["IRDPSRAPIAudioStream interface [RDP]","Start method","IRDPSRAPIAudioStream.Start","IRDPSRAPIAudioStream::Start","Start","Start method [RDP]","Start method [RDP]","IRDPSRAPIAudioStream interface","rdp.irdpsrapiaudiostream_start","rdpencomapi/IRDPSRAPIAudioStream::Start"]
old-location: rdp\irdpsrapiaudiostream_start.htm
tech.root: rdp
ms.assetid: 23ADA8F5-9F44-45E6-88DC-852D8F62F03F
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIAudioStream interface [RDP],Start method, IRDPSRAPIAudioStream.Start, IRDPSRAPIAudioStream::Start, Start, Start method [RDP], Start method [RDP],IRDPSRAPIAudioStream interface, rdp.irdpsrapiaudiostream_start, rdpencomapi/IRDPSRAPIAudioStream::Start
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
 - IRDPSRAPIAudioStream::Start
 - rdpencomapi/IRDPSRAPIAudioStream::Start
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
 - IRDPSRAPIAudioStream.Start
---

# IRDPSRAPIAudioStream::Start


## -description

Starts the audio stream. The audio stream must be initialized by calling the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-initialize">Initialize</a> method before it can be started.



## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiaudiostream">IRDPSRAPIAudioStream</a>



<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiaudiostream-initialize">Initialize</a>
