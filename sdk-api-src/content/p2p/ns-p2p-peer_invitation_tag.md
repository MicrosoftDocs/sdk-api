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
 

 

