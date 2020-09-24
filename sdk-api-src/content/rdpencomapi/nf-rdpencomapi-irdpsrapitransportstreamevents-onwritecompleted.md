---
UID: NF:rdpencomapi.IRDPSRAPITransportStreamEvents.OnWriteCompleted
title: IRDPSRAPITransportStreamEvents::OnWriteCompleted (rdpencomapi.h)
description: Notifies the Remote Desktop Protocol (RDP) stack that a write operation has completed.
helpviewer_keywords: ["IRDPSRAPITransportStreamEvents interface [RDP]","OnWriteCompleted method","IRDPSRAPITransportStreamEvents.OnWriteCompleted","IRDPSRAPITransportStreamEvents::OnWriteCompleted","OnWriteCompleted","OnWriteCompleted method [RDP]","OnWriteCompleted method [RDP]","IRDPSRAPITransportStreamEvents interface","rdp.irdpsrapitransportstreamevents_onwritecompleted","rdpencomapi/IRDPSRAPITransportStreamEvents::OnWriteCompleted"]
old-location: rdp\irdpsrapitransportstreamevents_onwritecompleted.htm
tech.root: rdp
ms.assetid: 19d99eba-e7ee-4bdc-8a9f-2cac97d17dea
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStreamEvents interface [RDP],OnWriteCompleted method, IRDPSRAPITransportStreamEvents.OnWriteCompleted, IRDPSRAPITransportStreamEvents::OnWriteCompleted, OnWriteCompleted, OnWriteCompleted method [RDP], OnWriteCompleted method [RDP],IRDPSRAPITransportStreamEvents interface, rdp.irdpsrapitransportstreamevents_onwritecompleted, rdpencomapi/IRDPSRAPITransportStreamEvents::OnWriteCompleted
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
 - IRDPSRAPITransportStreamEvents::OnWriteCompleted
 - rdpencomapi/IRDPSRAPITransportStreamEvents::OnWriteCompleted
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
 - IRDPSRAPITransportStreamEvents.OnWriteCompleted
---

# IRDPSRAPITransportStreamEvents::OnWriteCompleted


## -description

Notifies the Remote Desktop Protocol (RDP) stack that a write operation has completed. The RDP stack resumes ownership of the stream buffer and uses it for subsequent operations.

## -parameters

### -param pBuffer [in]

Type: <b><a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a>*</b>

An <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreambuffer">IRDPSRAPITransportStreamBuffer</a> interface pointer that represents the stream buffer that was written.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreamevents">IRDPSRAPITransportStreamEvents</a>



<a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapitransportstream-writebuffer">WriteBuffer</a>