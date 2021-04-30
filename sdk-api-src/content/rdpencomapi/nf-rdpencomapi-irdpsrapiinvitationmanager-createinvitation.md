---
UID: NF:rdpencomapi.IRDPSRAPIInvitationManager.CreateInvitation
title: IRDPSRAPIInvitationManager::CreateInvitation (rdpencomapi.h)
description: Creates an invitation.
helpviewer_keywords: ["CreateInvitation","CreateInvitation method [RDP]","CreateInvitation method [RDP]","IRDPSRAPIInvitationManager interface","IRDPSRAPIInvitationManager interface [RDP]","CreateInvitation method","IRDPSRAPIInvitationManager.CreateInvitation","IRDPSRAPIInvitationManager::CreateInvitation","rdp.irdpsrapiinvitationmanager_createinvitation","rdpencomapi/IRDPSRAPIInvitationManager::CreateInvitation"]
old-location: rdp\irdpsrapiinvitationmanager_createinvitation.htm
tech.root: rdp
ms.assetid: 169d220b-3a2a-490e-9c1c-03a707d59f6c
ms.date: 12/05/2018
ms.keywords: CreateInvitation, CreateInvitation method [RDP], CreateInvitation method [RDP],IRDPSRAPIInvitationManager interface, IRDPSRAPIInvitationManager interface [RDP],CreateInvitation method, IRDPSRAPIInvitationManager.CreateInvitation, IRDPSRAPIInvitationManager::CreateInvitation, rdp.irdpsrapiinvitationmanager_createinvitation, rdpencomapi/IRDPSRAPIInvitationManager::CreateInvitation
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
 - IRDPSRAPIInvitationManager::CreateInvitation
 - rdpencomapi/IRDPSRAPIInvitationManager::CreateInvitation
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
 - IRDPSRAPIInvitationManager.CreateInvitation
---

# IRDPSRAPIInvitationManager::CreateInvitation


## -description

Creates an invitation.

## -parameters

### -param bstrAuthString [in]

Type: <b>BSTR</b>

String to use for the authorization. The string is limited to 255 characters and must be unique for the session. If <b>NULL</b>, the method generates the string for you.

### -param bstrGroupName [in]

Type: <b>BSTR</b>

The name of the group. The string must be unique for the session. Applications typically use the group name to separate attendees into groups that can be granted different authorization levels.

### -param bstrPassword [in]

Type: <b>BSTR</b>

Password to use for authentication. The password is limited to 255 characters. You must provide the password to the viewer out-of-band from the ticket.

### -param AttendeeLimit [in]

Type: <b>long</b>

The maximum number of attendees.

### -param ppInvitation [out]

Type: <b>IRDPSRAPIInvitation**</b>

An <a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitation">IRDPSRAPIInvitation</a> interface pointer.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitationmanager">IRDPSRAPIInvitationManager</a>