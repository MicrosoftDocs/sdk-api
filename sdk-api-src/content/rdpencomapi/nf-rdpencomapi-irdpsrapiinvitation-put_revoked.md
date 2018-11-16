---
UID: NF:rdpencomapi.IRDPSRAPIInvitation.put_Revoked
title: IRDPSRAPIInvitation::put_Revoked
author: windows-sdk-content
description: The revoked state of the invitation.
old-location: rdp\irdpsrapiinvitation_revoked.htm
tech.root: Rdp
ms.assetid: a5a2d1a4-a51b-4fd4-b79c-3381f296d072
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IRDPSRAPIInvitation interface [RDP],Revoked property, IRDPSRAPIInvitation.Revoked, IRDPSRAPIInvitation.put_Revoked, IRDPSRAPIInvitation::Revoked, IRDPSRAPIInvitation::get_Revoked, IRDPSRAPIInvitation::put_Revoked, RDPSRAPIInvitation object [RDP],Revoked property, Revoked property [RDP], Revoked property [RDP],IRDPSRAPIInvitation interface, Revoked property [RDP],RDPSRAPIInvitation object, put_Revoked, rdp.irdpsrapiinvitation_revoked, rdpencomapi/IRDPSRAPIInvitation::Revoked, rdpencomapi/IRDPSRAPIInvitation::get_Revoked, rdpencomapi/IRDPSRAPIInvitation::put_Revoked
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IRDPSRAPIInvitation.Revoked
 - IRDPSRAPIInvitation.get_Revoked
 - IRDPSRAPIInvitation.put_Revoked
 - RDPSRAPIInvitation.Revoked
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- rdpencomapi.h
: 
- IRDPSRAPIInvitation.put_Revoked
: 
---

# IRDPSRAPIInvitation::put_Revoked


## -description


The revoked state of the invitation.

This property is read/write.


## -parameters


## -remarks



There is no way to delete an invitation, only to revoke it. This enables the application to check whether a ticket was issued before to ensure that each invitation has a unique ticket. If an invitation state is revoked,  no new attendees can connect by using that invitation.




## -see-also




<a href="https://msdn.microsoft.com/66cd8251-726a-4368-8da5-4d3f6899bdc8">IRDPSRAPIInvitation</a>
 

 

