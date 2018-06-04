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

# peer_member_change_type_tag enumeration


## -description



      The <b>PEER_MEMBER_CHANGE_TYPE</b> enumeration defines the set of possible peer group membership and presence states for a peer.


## -enum-fields




### -field PEER_MEMBER_CONNECTED

A member is connected to a peer group.


### -field PEER_MEMBER_DISCONNECTED

A member is disconnected from a peer group.


### -field PEER_MEMBER_UPDATED

A member has updated information (for example, a new address) within a peer group.


### -field PEER_MEMBER_JOINED

New membership information is published for a group member. The peer name of a peer group member is obtained from the <b>pwzIdentity</b> field of the <a href="https://msdn.microsoft.com/5ba37006-1ded-4996-a190-d789e5cc0755">PEER_EVENT_MEMBER_CHANGE_DATA</a>  structure. New membership information is published in one of the following three scenarios: 

<ul>
<li>An administrator calls <a href="https://msdn.microsoft.com/81284e61-fc31-47c3-a296-c9c02a2889ec">PeerGroupIssueCredentials</a> with the PEER_GROUP_STORE_CREDENTIALS flag set.</li>
<li>A user connects to a peer group for the first time, and the PEER_MEMBER_DATA_OPTIONAL flag is not set.</li>
<li>A peer group member performs an operation (for example, issuing an invitation or credentials, or publishing a record), but membership information for the peer group member does not exist in the group.</li>
</ul>

### -field PEER_MEMBER_LEFT

This peer event does not exist in the Peer Grouping Infrastructure v1.0, and must not be used.


## -see-also




<a href="https://msdn.microsoft.com/5ba37006-1ded-4996-a190-d789e5cc0755">
        PEER_EVENT_MEMBER_CHANGE_DATA</a>
 

 

