---
UID: NS:p2p.peer_application_tag
title: peer_application_tag
author: windows-sdk-content
description: The PEER_APPLICATION structure contains data describing a locally installed software application or component that can be registered and shared with trusted contacts within a peer collaboration network.
old-location: p2p\peer_application.htm
old-project: p2psdk
ms.assetid: a219231b-75d0-47d3-8294-f1cc25b43d27
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPEER_APPLICATION, PCPEER_APPLICATION, PCPEER_APPLICATION structure pointer [Peer Networking], PEER_APPLICATION, PEER_APPLICATION structure [Peer Networking], PPEER_APPLICATION, PPEER_APPLICATION structure pointer [Peer Networking], p2p.peer_application, p2p/PCPEER_APPLICATION, p2p/PEER_APPLICATION, p2p/PPEER_APPLICATION, peer_application_tag"
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
req.typenames: PEER_APPLICATION, *PPEER_APPLICATION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_APPLICATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_application_tag structure


## -description


The <b>PEER_APPLICATION</b> structure contains data describing a locally installed software application or component  that can be registered and shared with trusted contacts within a peer collaboration network.


## -struct-fields




### -field id

The GUID value under which the application is registered with the local computer.


### -field data


<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a> structure that contains the application information in a member byte buffer. This information is available to anyone who can query for the local peer's member information. This data is limited to 16K.


### -field pwzDescription

Pointer to a zero-terminated Unicode string that contains an optional  description of the local application. This description is limited to 255 unicode characters.


## -remarks



An "application" is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

A peer application has a GUID representing a single specific application. When an application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To deregister a peer application, call <a href="https://msdn.microsoft.com/2479b726-20f1-4370-9fcf-f29cec44c3ec">PeerCollabUnregisterApplication</a> with this GUID.




## -see-also




<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

