---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

