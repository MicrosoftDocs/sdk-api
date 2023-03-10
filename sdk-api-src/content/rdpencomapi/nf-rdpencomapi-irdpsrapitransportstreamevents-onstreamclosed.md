---
UID: NF:rdpencomapi.IRDPSRAPITransportStreamEvents.OnStreamClosed
title: IRDPSRAPITransportStreamEvents::OnStreamClosed (rdpencomapi.h)
description: Notifies the Remote Desktop Protocol (RDP) stack that the connection was closed.
helpviewer_keywords: ["IRDPSRAPITransportStreamEvents interface [RDP]","OnStreamClosed method","IRDPSRAPITransportStreamEvents.OnStreamClosed","IRDPSRAPITransportStreamEvents::OnStreamClosed","OnStreamClosed","OnStreamClosed method [RDP]","OnStreamClosed method [RDP]","IRDPSRAPITransportStreamEvents interface","rdp.irdpsrapitransportstreamevents_onstreamclosed","rdpencomapi/IRDPSRAPITransportStreamEvents::OnStreamClosed"]
old-location: rdp\irdpsrapitransportstreamevents_onstreamclosed.htm
tech.root: rdp
ms.assetid: 98767b91-95c1-4883-b27c-16c20d1da507
ms.date: 12/05/2018
ms.keywords: IRDPSRAPITransportStreamEvents interface [RDP],OnStreamClosed method, IRDPSRAPITransportStreamEvents.OnStreamClosed, IRDPSRAPITransportStreamEvents::OnStreamClosed, OnStreamClosed, OnStreamClosed method [RDP], OnStreamClosed method [RDP],IRDPSRAPITransportStreamEvents interface, rdp.irdpsrapitransportstreamevents_onstreamclosed, rdpencomapi/IRDPSRAPITransportStreamEvents::OnStreamClosed
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
 - IRDPSRAPITransportStreamEvents::OnStreamClosed
 - rdpencomapi/IRDPSRAPITransportStreamEvents::OnStreamClosed
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
 - IRDPSRAPITransportStreamEvents.OnStreamClosed
---

# IRDPSRAPITransportStreamEvents::OnStreamClosed


## -description

Notifies the Remote Desktop Protocol (RDP) stack that the connection was closed.

## -parameters

### -param hrReason [in]

Type: <b>HRESULT</b>

An <b>HRESULT</b> value that specifies if the stream was closed normally or due to an error. Contains <b>S_OK</b> if the stream was closed normally or an error code otherwise.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapitransportstreamevents">IRDPSRAPITransportStreamEvents</a>