---
UID: NF:rdpencomapi.IRDPSRAPIInvitation.put_Revoked
title: IRDPSRAPIInvitation::put_Revoked method
author: windows-driver-content
description: The revoked state of the invitation.
old-location: rdp\irdpsrapiinvitation_revoked.htm
old-project: Rdp
ms.assetid: a5a2d1a4-a51b-4fd4-b79c-3381f296d072
ms.author: windowsdriverdev
ms.date: 3/28/2018
ms.keywords: IRDPSRAPIInvitation, IRDPSRAPIInvitation interface [RDP], Revoked property, IRDPSRAPIInvitation.Revoked, IRDPSRAPIInvitation::get_Revoked, IRDPSRAPIInvitation::put_Revoked, RDPSRAPIInvitation object [RDP], Revoked property, Revoked property [RDP], Revoked property [RDP], IRDPSRAPIInvitation interface, Revoked property [RDP], RDPSRAPIInvitation object, put_Revoked,IRDPSRAPIInvitation.put_Revoked, rdp.irdpsrapiinvitation_revoked, rdpencomapi/IRDPSRAPIInvitation::Revoked, rdpencomapi/IRDPSRAPIInvitation::get_Revoked, rdpencomapi/IRDPSRAPIInvitation::put_Revoked
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: rdpencomapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: RdpEncomAPI.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: RdpEncomAPI.tlb
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	RdpEncom.dll
api_name:
-	IRDPSRAPIInvitation.Revoked
-	IRDPSRAPIInvitation.get_Revoked
-	IRDPSRAPIInvitation.put_Revoked
-	RDPSRAPIInvitation.Revoked
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# IRDPSRAPIInvitation::put_Revoked method


## -description


The revoked state of the invitation.

This property is read/write.


## -parameters


## -remarks



There is no way to delete an invitation, only to revoke it. This enables the application to check whether a ticket was issued before to ensure that each invitation has a unique ticket. If an invitation state is revoked,  no new attendees can connect by using that invitation.




## -see-also




<a href="https://msdn.microsoft.com/66cd8251-726a-4368-8da5-4d3f6899bdc8">IRDPSRAPIInvitation</a>
 

 

