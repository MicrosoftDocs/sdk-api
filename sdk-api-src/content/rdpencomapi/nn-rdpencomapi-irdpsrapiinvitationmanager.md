---
UID: NN:rdpencomapi.IRDPSRAPIInvitationManager
title: IRDPSRAPIInvitationManager (rdpencomapi.h)
description: Manages invitation objects.
helpviewer_keywords: ["IRDPSRAPIInvitationManager","IRDPSRAPIInvitationManager interface [RDP]","IRDPSRAPIInvitationManager interface [RDP]","described","rdp.irdpsrapiinvitationmanager","rdpencomapi/IRDPSRAPIInvitationManager"]
old-location: rdp\irdpsrapiinvitationmanager.htm
tech.root: rdp
ms.assetid: 300940ef-e8a6-4dd9-a078-d4325e20ae91
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIInvitationManager, IRDPSRAPIInvitationManager interface [RDP], IRDPSRAPIInvitationManager interface [RDP],described, rdp.irdpsrapiinvitationmanager, rdpencomapi/IRDPSRAPIInvitationManager
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
 - IRDPSRAPIInvitationManager
 - rdpencomapi/IRDPSRAPIInvitationManager
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
 - IRDPSRAPIInvitationManager
---

# IRDPSRAPIInvitationManager interface


## -description

Manages invitation objects.

Applications obtain access to this object using <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapisharingsession-get_invitations">IRDPSRAPISharingSession::get_Invitations</a>


This interface provides access to the <b>RDPSRAPIInvitationManager</b> object.

## -inheritance

The <b>IRDPSRAPIInvitationManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IRDPSRAPIInvitationManager</b> also has these types of members:

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitation">IRDPSRAPIInvitation</a>
