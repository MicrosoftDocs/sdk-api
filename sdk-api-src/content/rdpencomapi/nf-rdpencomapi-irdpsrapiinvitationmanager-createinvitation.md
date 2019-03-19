---
UID: NF:rdpencomapi.IRDPSRAPIInvitationManager.CreateInvitation
title: IRDPSRAPIInvitationManager::CreateInvitation (rdpencomapi.h)
author: windows-sdk-content
description: Creates an invitation.
old-location: rdp\irdpsrapiinvitationmanager_createinvitation.htm
tech.root: rdp
ms.assetid: 169d220b-3a2a-490e-9c1c-03a707d59f6c
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CreateInvitation, CreateInvitation method [RDP], CreateInvitation method [RDP],IRDPSRAPIInvitationManager interface, IRDPSRAPIInvitationManager interface [RDP],CreateInvitation method, IRDPSRAPIInvitationManager.CreateInvitation, IRDPSRAPIInvitationManager::CreateInvitation, rdp.irdpsrapiinvitationmanager_createinvitation, rdpencomapi/IRDPSRAPIInvitationManager::CreateInvitation
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIInvitationManager.CreateInvitation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

An <a href="https://msdn.microsoft.com/66cd8251-726a-4368-8da5-4d3f6899bdc8">IRDPSRAPIInvitation</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the return value is an error code.




## -see-also




<a href="https://msdn.microsoft.com/300940ef-e8a6-4dd9-a078-d4325e20ae91">IRDPSRAPIInvitationManager</a>
 

 

