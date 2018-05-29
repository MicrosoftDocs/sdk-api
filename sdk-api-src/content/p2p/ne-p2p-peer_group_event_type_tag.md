---
UID: NE:p2p.peer_group_event_type_tag
title: peer_group_event_type_tag
author: windows-sdk-content
description: The PEER_GROUP_EVENT_TYPE enumeration contains the specific peer event types that can occur within a peer group.
old-location: p2p\peer_group_event_type.htm
old-project: P2PSdk
ms.assetid: 9c28eb24-f158-4313-9a7c-0f271013d03a
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PEER_GROUP_EVENT_CONNECTION_FAILED, PEER_GROUP_EVENT_DIRECT_CONNECTION, PEER_GROUP_EVENT_INCOMING_DATA, PEER_GROUP_EVENT_MEMBER_CHANGED, PEER_GROUP_EVENT_NEIGHBOR_CONNECTION, PEER_GROUP_EVENT_PROPERTY_CHANGED, PEER_GROUP_EVENT_RECORD_CHANGED, PEER_GROUP_EVENT_STATUS_CHANGED, PEER_GROUP_EVENT_TYPE, PEER_GROUP_EVENT_TYPE enumeration [Peer Networking], p2p.peer_group_event_type, p2p/ PEER_GROUP_EVENT_TYPE, p2p/PEER_GROUP_EVENT_CONNECTION_FAILED, p2p/PEER_GROUP_EVENT_DIRECT_CONNECTION, p2p/PEER_GROUP_EVENT_INCOMING_DATA, p2p/PEER_GROUP_EVENT_MEMBER_CHANGED, p2p/PEER_GROUP_EVENT_NEIGHBOR_CONNECTION, p2p/PEER_GROUP_EVENT_PROPERTY_CHANGED, p2p/PEER_GROUP_EVENT_RECORD_CHANGED, p2p/PEER_GROUP_EVENT_STATUS_CHANGED, peer_group_event_type_tag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1with the Advanced Networking Pack forWindows XP
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
req.typenames: PEER_GROUP_EVENT_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_GROUP_EVENT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_group_event_type_tag enumeration


## -description



      The <b>PEER_GROUP_EVENT_TYPE</b> enumeration contains the specific peer event types that can occur within a peer group.


## -enum-fields




### -field PEER_GROUP_EVENT_STATUS_CHANGED

The status of the group has changed. This peer event is fired when one of the flags listed in the <a href="https://msdn.microsoft.com/ed3fa9a6-5180-419f-b5d1-02889bbcdd0d">PEER_GROUP_STATUS</a> enumeration are set or changed for the group.


### -field PEER_GROUP_EVENT_PROPERTY_CHANGED

A member in the <a href="https://msdn.microsoft.com/a1501343-bd84-4dbe-91d0-c64c59e34abc">PEER_GROUP_PROPERTIES</a> structure has changed.   The application already has the change and must use <a href="https://msdn.microsoft.com/6273817f-9698-4c0b-93a9-9bbee2e5dc78">PeerGroupGetProperties</a> to get the updated structure. This peer event does not have associated data present in <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a> to retrieve.


### -field PEER_GROUP_EVENT_RECORD_CHANGED

A group record has changed. Information on this change is provided in the <b>recordChangeData</b> member of <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_DIRECT_CONNECTION

The status of a direct connection has changed. Information on this change is provided in the <b>connectionChangeData</b> member of <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_NEIGHBOR_CONNECTION

The status of a neighbor connection has changed. Information on this change is provided in the <b>connectionChangeData</b>  member of <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_INCOMING_DATA

Incoming direct connection data from a member is detected. Information on this peer event is provided in the <b>incomingData</b>  member of <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_MEMBER_CHANGED

The status of a member has changed. Information on this change is provided in the <b>memberChangeData</b>  member of <a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">PEER_GROUP_EVENT_DATA</a>.


### -field PEER_GROUP_EVENT_CONNECTION_FAILED

The connection to the peer group has failed. No data is provided when this peer event is raised. This event is also raised if no members are online in a group you are attempting to connect to for the first time. 



### -field PEER_GROUP_EVENT_AUTHENTICATION_FAILED




## -see-also




<a href="https://msdn.microsoft.com/5cdae832-e6a7-481c-9784-1c1c07d689dd">
        PEER_GROUP_EVENT_DATA</a>



<a href="https://msdn.microsoft.com/9c9c82c3-b02a-49c2-9a8f-eb355ded8480">
        PEER_GROUP_EVENT_REGISTRATION</a>
 

 

