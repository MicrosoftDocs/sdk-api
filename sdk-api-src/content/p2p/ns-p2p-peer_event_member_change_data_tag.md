---
UID: NS:p2p.peer_event_member_change_data_tag
title: peer_event_member_change_data_tag
author: windows-sdk-content
description: The PEER_EVENT_MEMBER_CHANGE_DATA structure contains data that describes a change in the status of a peer group member.
old-location: p2p\peer_event_member_change_data.htm
old-project: P2PSdk
ms.assetid: 5ba37006-1ded-4996-a190-d789e5cc0755
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_EVENT_MEMBER_CHANGE_DATA, PEER_EVENT_MEMBER_CHANGE_DATA, PEER_EVENT_MEMBER_CHANGE_DATA structure [Peer Networking], PPEER_EVENT_MEMBER_CHANGE_DATA, PPEER_EVENT_MEMBER_CHANGE_DATA structure pointer [Peer Networking], p2p.peer_event_member_change_data, p2p/PPEER_EVENT_MEMBER_CHANGE_DATA, p2p/peer_event_member_change_data_tag, peer_event_member_change_data_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: PEER_EVENT_MEMBER_CHANGE_DATA, *PPEER_EVENT_MEMBER_CHANGE_DATA
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_EVENT_MEMBER_CHANGE_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_event_member_change_data_tag structure


## -description


The <b>PEER_EVENT_MEMBER_CHANGE_DATA</b> structure contains data that describes a change in the status of a peer group member.


## -struct-fields




### -field dwSize

Contains the size of this structure, in bytes.


### -field changeType

<b>PEER_MEMBER_CHANGE_TYPE</b> enumeration value that specifies the change event that occurred, such as a member joining or leaving.


### -field pwzIdentity

Pointer to a Unicode string that contains the peer name of the peer group member.


## -see-also




<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/9c9c82c3-b02a-49c2-9a8f-eb355ded8480">PEER_GROUP_EVENT_REGISTRATION</a>



<a href="https://msdn.microsoft.com/ecebec4f-1dc6-481c-a2d4-cf0043729a8c">PEER_MEMBER_CHANGE_TYPE</a>
 

 

