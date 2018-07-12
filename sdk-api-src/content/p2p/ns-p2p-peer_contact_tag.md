---
UID: NS:p2p.peer_contact_tag
title: peer_contact_tag
author: windows-sdk-content
description: The PEER_CONTACT structure contains information about a specific contact.
old-location: p2p\peer_contact.htm
old-project: p2psdk
ms.assetid: b84a17fc-35d6-4098-9bb3-18e708541a80
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: "*PPEER_CONTACT, PCPEER_CONTACT, PCPEER_CONTACT structure pointer [Peer Networking], PEER_CONTACT, PEER_CONTACT structure [Peer Networking], PPEER_CONTACT, PPEER_CONTACT structure pointer [Peer Networking], p2p.peer_contact, p2p/PCPEER_CONTACT, p2p/PEER_CONTACT, p2p/PPEER_CONTACT, peer_contact_tag"
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
req.typenames: PEER_CONTACT, *PPEER_CONTACT
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_CONTACT
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_contact_tag structure


## -description


The <b>PEER_CONTACT</b> structure contains information about a specific contact.


## -struct-fields




### -field pwzPeerName

Zero-terminated Unicode string that contains the peer name of the contact. This is the unique identifier for a contact.  There can only be a single contact associated with any given peername.


### -field pwzNickName

Zero-terminated Unicode string that contains the nickname of the contact and can be modified at any time. This is used when the peer collaboration scope is set to People Near Me. It is advertised in People Near Me and seen by recipients of sent invitations. 

This member is limited to 255 unicode characters.


### -field pwzDisplayName

Zero-terminated Unicode string that contains the display name of the contact. This corresponds to the display name seen for the contact in a peer's contacts folder.

This member is limited to 255 unicode characters.


### -field pwzEmailAddress

Zero-terminated Unicode string that contains the email address of the contact.


### -field fWatch

If true, the contact is watched by the peer; if false, it is not.


### -field WatcherPermissions


<a href="https://msdn.microsoft.com/e3f4a1e6-6ac8-48f8-8480-0cf60c9b4ce9">PEER_WATCH_PERMISSION</a> enumeration value that specifies the watch permissions for this contact.


### -field credentials


<a href="https://msdn.microsoft.com/d8a8b9e3-c455-4813-b812-263efe7f5e3e">PEER_DATA</a> structure that contains the security credentials for the contact in an opaque byte buffer.


## -remarks



"Contacts" are peers participating in a peer collaboration network who publish presence information available to the local peer. This associated information enables the peer application to "watch" them for updates and peer application or object status changes. Lists of contacts are maintained by the peer collaboration infrastructure, and specific status change events are raised for each individual contact in the list.




## -see-also




<a href="https://msdn.microsoft.com/e3f4a1e6-6ac8-48f8-8480-0cf60c9b4ce9">PEER_WATCH_PERMISSION</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

