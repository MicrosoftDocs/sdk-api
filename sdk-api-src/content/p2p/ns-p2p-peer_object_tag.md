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

# peer_object_tag structure


## -description


The <b>PEER_OBJECT</b> structure contains application-specific run-time information that can be shared with trusted contacts within a peer collaboration network.


## -struct-fields




### -field id

GUID value under which the peer object is uniquely registered.


### -field data


<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a> structure that contains information which describes the peer object.


### -field dwPublicationScope


<a href="https://msdn.microsoft.com/fecb9403-f790-4955-a879-fb3e6fbfe8ca">PEER_PUBLICATION_SCOPE</a> enumeration value that specifies the publication scope for this peer object.


## -remarks



Peer objects are run-time data items associated with a particular application, such as a picture or avatar, a certificate, or a specific description. Each peer object must be smaller than 16K in size.

Trusted contacts watching this peer object will have a PEER_EVENT_OBJECT_CHANGED event raised on them signaling this peer object's change in status.

Peer object information is contained in the <b>data</b> member of this structure and  represented as a byte buffer with a maximum size of 16K.

The lifetime of a peer object is tied to the lifetime of the application that registered it.




## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

