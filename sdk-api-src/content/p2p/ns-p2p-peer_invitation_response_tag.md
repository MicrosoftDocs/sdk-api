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

# peer_invitation_response_tag structure


## -description


The <b>PEER_INVITATION_RESPONSE</b> structure contains a response to an invitation to join a peer collaboration activity.


## -struct-fields




### -field action


<a href="https://msdn.microsoft.com/ad456eb5-a28c-4826-976f-e38e2f269ff0">PEER_INVITATION_RESPONSE_TYPE</a> enumeration value that specifies the action the peer takes in response to the invitation.


### -field pwzMessage

Reserved. This member must be set to <b>NULL</b>, and is set exclusively by the Peer Collaboration infrastructure.


### -field hrExtendedInfo

Any extended information that is part of the response. This can include an error code corresponding to the failure on the recipient of the invitation.


## -see-also




<a href="https://msdn.microsoft.com/b74b45c0-760f-4008-87dd-9fdea0d4be05">PEER_INVITATION</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

