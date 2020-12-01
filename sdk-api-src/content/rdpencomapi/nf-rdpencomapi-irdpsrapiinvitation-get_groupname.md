---
UID: NF:rdpencomapi.IRDPSRAPIInvitation.get_GroupName
title: IRDPSRAPIInvitation::get_GroupName (rdpencomapi.h)
description: The group name.
helpviewer_keywords: ["GroupName property [RDP]","GroupName property [RDP]","IRDPSRAPIInvitation interface","GroupName property [RDP]","RDPSRAPIInvitation object","IRDPSRAPIInvitation interface [RDP]","GroupName property","IRDPSRAPIInvitation.GroupName","IRDPSRAPIInvitation.get_GroupName","IRDPSRAPIInvitation::GroupName","IRDPSRAPIInvitation::get_GroupName","RDPSRAPIInvitation object [RDP]","GroupName property","get_GroupName","rdp.irdpsrapiinvitation_groupname","rdpencomapi/IRDPSRAPIInvitation::GroupName","rdpencomapi/IRDPSRAPIInvitation::get_GroupName"]
old-location: rdp\irdpsrapiinvitation_groupname.htm
tech.root: rdp
ms.assetid: 7ac76417-bb5c-40ae-a22a-b322b42b0d2c
ms.date: 12/05/2018
ms.keywords: GroupName property [RDP], GroupName property [RDP],IRDPSRAPIInvitation interface, GroupName property [RDP],RDPSRAPIInvitation object, IRDPSRAPIInvitation interface [RDP],GroupName property, IRDPSRAPIInvitation.GroupName, IRDPSRAPIInvitation.get_GroupName, IRDPSRAPIInvitation::GroupName, IRDPSRAPIInvitation::get_GroupName, RDPSRAPIInvitation object [RDP],GroupName property, get_GroupName, rdp.irdpsrapiinvitation_groupname, rdpencomapi/IRDPSRAPIInvitation::GroupName, rdpencomapi/IRDPSRAPIInvitation::get_GroupName
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
 - IRDPSRAPIInvitation::get_GroupName
 - rdpencomapi/IRDPSRAPIInvitation::get_GroupName
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
 - IRDPSRAPIInvitation.GroupName
 - IRDPSRAPIInvitation.get_GroupName
 - RDPSRAPIInvitation.GroupName
---

# IRDPSRAPIInvitation::get_GroupName


## -description

The group name.

This property is read-only.

## -parameters

## -remarks

The group name is set when calling the <a href="/windows/desktop/api/rdpencomapi/nf-rdpencomapi-irdpsrapiinvitationmanager-createinvitation">IRDPSRAPIInvitationManager::CreateInvitation</a> method. Applications typically use this property to separate attendees into groups that can be granted different authorization levels.

## -see-also

<a href="/windows/desktop/api/rdpencomapi/nn-rdpencomapi-irdpsrapiinvitation">IRDPSRAPIInvitation</a>