---
UID: NS:p2p.peer_contact_tag
title: PEER_CONTACT (p2p.h)
description: The PEER_CONTACT structure contains information about a specific contact.
helpviewer_keywords: ["*PPEER_CONTACT","PCPEER_CONTACT","PCPEER_CONTACT structure pointer [Peer Networking]","PEER_CONTACT","PEER_CONTACT structure [Peer Networking]","PPEER_CONTACT","PPEER_CONTACT structure pointer [Peer Networking]","p2p.peer_contact","p2p/PCPEER_CONTACT","p2p/PEER_CONTACT","p2p/PPEER_CONTACT"]
old-location: p2p\peer_contact.htm
tech.root: p2p
ms.assetid: b84a17fc-35d6-4098-9bb3-18e708541a80
ms.date: 12/05/2018
ms.keywords: '*PPEER_CONTACT, PCPEER_CONTACT, PCPEER_CONTACT structure pointer [Peer Networking], PEER_CONTACT, PEER_CONTACT structure [Peer Networking], PPEER_CONTACT, PPEER_CONTACT structure pointer [Peer Networking], p2p.peer_contact, p2p/PCPEER_CONTACT, p2p/PEER_CONTACT, p2p/PPEER_CONTACT'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PEER_CONTACT, *PPEER_CONTACT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_contact_tag
 - p2p/peer_contact_tag
 - PPEER_CONTACT
 - p2p/PPEER_CONTACT
 - PEER_CONTACT
 - p2p/PEER_CONTACT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_CONTACT
---

# PEER_CONTACT structure


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

<a href="/windows/desktop/api/p2p/ne-p2p-peer_watch_permission">PEER_WATCH_PERMISSION</a> enumeration value that specifies the watch permissions for this contact.

### -field credentials

<a href="/windows/desktop/api/p2p/ns-p2p-peer_data">PEER_DATA</a> structure that contains the security credentials for the contact in an opaque byte buffer.

## -remarks

"Contacts" are peers participating in a peer collaboration network who publish presence information available to the local peer. This associated information enables the peer application to "watch" them for updates and peer application or object status changes. Lists of contacts are maintained by the peer collaboration infrastructure, and specific status change events are raised for each individual contact in the list.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_watch_permission">PEER_WATCH_PERMISSION</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>