---
UID: NE:p2p.peer_member_flags_tag
title: PEER_MEMBER_FLAGS (p2p.h)
description: The PEER_MEMBER_FLAGS flag allows an application to specify whether all members or only present ones should be enumerated when the PeerGroupEnumMembers function is called, or to indicate whether or not a member is present within the peer group.
helpviewer_keywords: ["PEER_MEMBER_FLAGS","PEER_MEMBER_FLAGS enumeration [Peer Networking]","PEER_MEMBER_PRESENT","p2p.peer_member_flags","p2p/PEER_MEMBER_FLAGS","p2p/PEER_MEMBER_PRESENT"]
old-location: p2p\peer_member_flags.htm
tech.root: p2p
ms.assetid: 96a8e4ae-dce6-4f07-ab22-71da347ef347
ms.date: 12/05/2018
ms.keywords: PEER_MEMBER_FLAGS, PEER_MEMBER_FLAGS enumeration [Peer Networking], PEER_MEMBER_PRESENT, p2p.peer_member_flags, p2p/PEER_MEMBER_FLAGS, p2p/PEER_MEMBER_PRESENT
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1with the Advanced Networking Pack forWindows XP
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
req.typenames: PEER_MEMBER_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_member_flags_tag
 - p2p/peer_member_flags_tag
 - PEER_MEMBER_FLAGS
 - p2p/PEER_MEMBER_FLAGS
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
 - PEER_MEMBER_FLAGS
---

# PEER_MEMBER_FLAGS enumeration


## -description

The <b>PEER_MEMBER_FLAGS</b> flag allows an application to specify whether all members or only present ones should be enumerated when the <a href="/windows/desktop/api/p2p/nf-p2p-peergroupenummembers">PeerGroupEnumMembers</a> function is called, or to indicate whether or not a member is present within the peer group.

## -enum-fields

### -field PEER_MEMBER_PRESENT:0x0001

The member is present in the peer group.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergroupenummembers">PeerGroupEnumMembers</a>
