---
UID: NF:rdpencomapi.IRDPSRAPISharingSession.ConnectToClient
title: IRDPSRAPISharingSession::ConnectToClient (rdpencomapi.h)
description: Used for reverse connect mode, where the sharer connects to the viewer.
helpviewer_keywords: ["ConnectToClient","ConnectToClient method [RDP]","ConnectToClient method [RDP]","IRDPSRAPISharingSession interface","ConnectToClient method [RDP]","IRDPSRAPISharingSession2 interface","IRDPSRAPISharingSession interface [RDP]","ConnectToClient method","IRDPSRAPISharingSession.ConnectToClient","IRDPSRAPISharingSession2 interface [RDP]","ConnectToClient method","IRDPSRAPISharingSession2::ConnectToClient","IRDPSRAPISharingSession::ConnectToClient","rdp.irdpsrapisharingsession_connecttoclient","rdpencomapi/IRDPSRAPISharingSession2::ConnectToClient","rdpencomapi/IRDPSRAPISharingSession::ConnectToClient"]
old-location: rdp\irdpsrapisharingsession_connecttoclient.htm
tech.root: rdp
ms.assetid: 18651433-90cb-4ebd-afaf-480800dfe033
ms.date: 12/05/2018
ms.keywords: ConnectToClient, ConnectToClient method [RDP], ConnectToClient method [RDP],IRDPSRAPISharingSession interface, ConnectToClient method [RDP],IRDPSRAPISharingSession2 interface, IRDPSRAPISharingSession interface [RDP],ConnectToClient method, IRDPSRAPISharingSession.ConnectToClient, IRDPSRAPISharingSession2 interface [RDP],ConnectToClient method, IRDPSRAPISharingSession2::ConnectToClient, IRDPSRAPISharingSession::ConnectToClient, rdp.irdpsrapisharingsession_connecttoclient, rdpencomapi/IRDPSRAPISharingSession2::ConnectToClient, rdpencomapi/IRDPSRAPISharingSession::ConnectToClient
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
 - IRDPSRAPISharingSession::ConnectToClient
 - rdpencomapi/IRDPSRAPISharingSession::ConnectToClient
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
 - IRDPSRAPISharingSession2.ConnectToClient
 - IRDPSRAPISharingSession.ConnectToClient
---

# IRDPSRAPISharingSession::ConnectToClient


## -description

Used for reverse connect mode, where the sharer  connects to the viewer. In this mode, the sharer sends the invitation file to the viewer out-of-band by using  instant messaging (IM) or email. For the sharer to connect to the viewer, the sharer receives a connection string from the viewer out-of-band through IM or email.

## -parameters

### -param bstrConnectionString [in]

Type: <b>BSTR</b>

Connection string that the viewer sends to the sharer out-of-band through IM or email.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession">IRDPSRAPISharingSession</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapisharingsession2">IRDPSRAPISharingSession2</a>