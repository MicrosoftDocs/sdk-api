---
UID: NF:rdpencomapi.IRDPSRAPITransportStreamEvents.OnReadCompleted
title: IRDPSRAPITransportStreamEvents::OnReadCompleted (rdpencomapi.h)
description: Notifies the Remote Desktop Protocol (RDP) stack that a read operation has completed.
helpviewer_keywords: ["IRDPSRAPITransportStreamEvents interface [RDP]","OnReadCompleted method","IRDPSRAPITransportStreamEvents.OnReadCompleted","IRDPSRAPITransportStreamEvents::OnReadCompleted","OnReadCompleted","OnReadCompleted method [RDP]","OnReadCompleted method [RDP]","IRDPSRAPITransportStreamEvents interface","rdp.irdpsrapitransportstreamevents_onreadcompleted","rdpencomapi/IRDPSRAPITransportStreamEvents::OnReadCompleted"]
old-location: rdp\irdpsrapitransportstreamevents_onreadcompleted.htm
tech.root: rdp
ms.assetid: 27c3a16a-3d78-46b1-b328-1a1b6f059687
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStreamEvents interface [RDP],OnReadCompleted method, IRDPSRAPITransportStreamEvents.OnReadCompleted, IRDPSRAPITransportStreamEvents::OnReadCompleted, OnReadCompleted, OnReadCompleted method [RDP], OnReadCompleted method [RDP],IRDPSRAPITransportStreamEvents interface, rdp.irdpsrapitransportstreamevents_onreadcompleted, rdpencomapi/IRDPSRAPITransportStreamEvents::OnReadCompleted
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
 - IRDPSRAPITransportStreamEvents::OnReadCompleted
 - rdpencomapi/IRDPSRAPITransportStreamEvents::OnReadCompleted
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
 - IRDPSRAPITransportStreamEvents.OnReadCompleted
---

# IRDPSRAPITransportStreamEvents::OnReadCompleted


## -description

Notifies the Remote Desktop Protocol (RDP) stack that a read operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.

## -parameters

### -param pBuffer [in]

Type: <b><a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the stream buffer that was read.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreamevents">IRDPSRAPITransportStreamEvents</a>



<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-readbuffer">ReadBuffer</a>