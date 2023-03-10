---
UID: NN:rdpencomapi.IRDPSRAPIInvitation
title: IRDPSRAPIInvitation (rdpencomapi.h)
description: Invitations enable a person or group of persons to connect to a session. When an attendee connects to a session, the client sends a ticket and a password. These two pieces of information are used to authenticate an attendee.
helpviewer_keywords: ["IRDPSRAPIInvitation","IRDPSRAPIInvitation interface [RDP]","IRDPSRAPIInvitation interface [RDP]","described","rdp.irdpsrapiinvitation","rdpencomapi/IRDPSRAPIInvitation"]
old-location: rdp\irdpsrapiinvitation.htm
tech.root: rdp
ms.assetid: 66cd8251-726a-4368-8da5-4d3f6899bdc8
ms.date: 12/05/2018
ms.keywords: IRDPSRAPIInvitation, IRDPSRAPIInvitation interface [RDP], IRDPSRAPIInvitation interface [RDP],described, rdp.irdpsrapiinvitation, rdpencomapi/IRDPSRAPIInvitation
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
 - IRDPSRAPIInvitation
 - rdpencomapi/IRDPSRAPIInvitation
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
 - IRDPSRAPIInvitation
---

# IRDPSRAPIInvitation interface


## -description

Invitations enable a person or group of persons to connect to a session. When an attendee connects to a session, the client sends a ticket and a password. These two pieces of information are used to authenticate an attendee.

Applications obtain access to this object using <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitationmanager-createinvitation">IRDPSRAPIInvitationManager::CreateInvitation</a>.

An attendee can join a session if the invitation list contains and invitation with the following properties:
<ul>
<li>The ticket string in <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitation-get_connectionstring">ConnectionString</a> matches the one sent by the client.</li>
<li>The password string in <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitation-get_password">Password</a> matches the one sent by the client.</li>
<li>The number of attendees has not exceeded the maximum number in <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitation-get_attendeelimit">AttendeeLimit</a>.</li>
<li>The invitation has not been revoked using <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitation-get_revoked">Revoked</a>.</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>



<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitationmanager">IRDPSRAPIInvitationManager</a>