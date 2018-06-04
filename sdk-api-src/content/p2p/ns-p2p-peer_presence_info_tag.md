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

# peer_presence_info_tag structure


## -description


The <b>PEER_PRESENCE_INFO</b> structure contains specific peer presence information.


## -struct-fields




### -field status


<a href="https://msdn.microsoft.com/0f7f6fa8-5da4-4f59-b9ea-0117ff8a3e28">PEER_PRESENCE_STATUS</a> enumeration value that indicates the current availability or level of participation by the peer in a peer collaboration network.


### -field pwzDescriptiveText

Zero-terminated Unicode string that contains a user- or application-defined message that expands upon the current status value. This string is limited to 255 characters.


## -remarks



Peer "presence" is information about a specific peer's level of participation in a peer collaboration network, such as whether or not the peer has logged into or out of the peer collaboration network, or has set a specific status (for example, "Busy, "Away").




## -see-also




<a href="https://msdn.microsoft.com/0f7f6fa8-5da4-4f59-b9ea-0117ff8a3e28">PEER_PRESENCE_STATUS</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

