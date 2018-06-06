---
UID: NS:p2p.peer_invitation_tag
title: peer_invitation_tag
author: windows-sdk-content
description: The PEER_INVITATION structure contains a request to initiate or join a peer collaboration activity.
old-location: p2p\peer_invitation.htm
old-project: P2PSdk
ms.assetid: b74b45c0-760f-4008-87dd-9fdea0d4be05
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_INVITATION, PEER_INVITATION, PEER_INVITATION structure [Peer Networking], PPEER_INVITATION, PPEER_INVITATION structure pointer [Peer Networking], p2p.peer_invitation, p2p/PEER_INVITATION, p2p/PPEER_INVITATION, peer_invitation_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
req.typenames: PEER_INVITATION, *PPEER_INVITATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_INVITATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_invitation_tag structure


## -description


The <b>PEER_INVITATION</b> structure contains a request to initiate or join a peer collaboration activity.


## -struct-fields




### -field applicationId

GUID value that uniquely identifies the registered software or software component for the peer collaboration activity.


### -field applicationData


<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a> structure that contains opaque data describing possible additional application-specific settings (for example, an address and port on which the activity will occur, or a specific video codec to use). This data is limited to 16K.


### -field pwzMessage

Zero-terminated Unicode string that contains a specific request message to the invitation recipient. The message is limited to 255 unicode characters.


## -remarks



An invitation request is typically sent by a peer after a contact appears online within the peer collaboration network and a call to <a href="https://msdn.microsoft.com/550cbd9d-5569-485e-897d-73d8bab8430a">PeerCollabEnumApplications</a> returns a common software application (represented as a application GUID) available on the contact's endpoint.




## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

