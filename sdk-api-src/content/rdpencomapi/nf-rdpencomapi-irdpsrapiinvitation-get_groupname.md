---
UID: NF:rdpencomapi.IRDPSRAPIInvitation.get_GroupName
title: IRDPSRAPIInvitation::get_GroupName
author: windows-sdk-content
description: The group name.
old-location: rdp\irdpsrapiinvitation_groupname.htm
old-project: Rdp
ms.assetid: 7ac76417-bb5c-40ae-a22a-b322b42b0d2c
ms.author: windowssdkdev
ms.date: 03/28/2018
ms.keywords: GroupName property [RDP], GroupName property [RDP],IRDPSRAPIInvitation interface, GroupName property [RDP],RDPSRAPIInvitation object, IRDPSRAPIInvitation interface [RDP],GroupName property, IRDPSRAPIInvitation.GroupName, IRDPSRAPIInvitation.get_GroupName, IRDPSRAPIInvitation::GroupName, IRDPSRAPIInvitation::get_GroupName, RDPSRAPIInvitation object [RDP],GroupName property, get_GroupName, rdp.irdpsrapiinvitation_groupname, rdpencomapi/IRDPSRAPIInvitation::GroupName, rdpencomapi/IRDPSRAPIInvitation::get_GroupName
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: RDPENCOMAPI_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - RdpEncom.dll
api_name:
 - IRDPSRAPIInvitation.GroupName
 - IRDPSRAPIInvitation.get_GroupName
 - RDPSRAPIInvitation.GroupName
product: Windows
targetos: Windows
req.lib: 
req.dll: RdpEncom.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IRDPSRAPIInvitation::get_GroupName


## -description


The group name.

This property is read-only.


## -parameters


## -remarks



The group name is set when calling the <a href="https://msdn.microsoft.com/169d220b-3a2a-490e-9c1c-03a707d59f6c">IRDPSRAPIInvitationManager::CreateInvitation</a> method. Applications typically use this property to separate attendees into groups that can be granted different authorization levels.




## -see-also




<a href="https://msdn.microsoft.com/66cd8251-726a-4368-8da5-4d3f6899bdc8">IRDPSRAPIInvitation</a>
 

 

