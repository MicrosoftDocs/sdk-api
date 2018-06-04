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
 

 

