---
UID: NE:p2p.peer_record_flags_tag
title: PEER_RECORD_FLAGS (p2p.h)
description: The PEER_RECORD_FLAGS enumeration specifies a set of flags for peer record behaviors.
helpviewer_keywords: ["PEER_RECORD_FLAGS","PEER_RECORD_FLAGS enumeration [Peer Networking]","PEER_RECORD_FLAG_AUTOREFRESH","PEER_RECORD_FLAG_DELETED","p2p.peer_record_flags","p2p/PEER_RECORD_FLAGS","p2p/PEER_RECORD_FLAG_AUTOREFRESH","p2p/PEER_RECORD_FLAG_DELETED"]
old-location: p2p\peer_record_flags.htm
tech.root: p2p
ms.assetid: 2ae2411d-3409-442a-8655-e54a34bf3938
ms.date: 12/05/2018
ms.keywords: PEER_RECORD_FLAGS, PEER_RECORD_FLAGS enumeration [Peer Networking], PEER_RECORD_FLAG_AUTOREFRESH, PEER_RECORD_FLAG_DELETED, p2p.peer_record_flags, p2p/PEER_RECORD_FLAGS, p2p/PEER_RECORD_FLAG_AUTOREFRESH, p2p/PEER_RECORD_FLAG_DELETED
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
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
req.typenames: PEER_RECORD_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_record_flags_tag
 - p2p/peer_record_flags_tag
 - PEER_RECORD_FLAGS
 - p2p/PEER_RECORD_FLAGS
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
 - PEER_RECORD_FLAGS
---

# PEER_RECORD_FLAGS enumeration


## -description

The <b>PEER_RECORD_FLAGS</b> enumeration specifies a set of flags for peer record behaviors.

## -enum-fields

### -field PEER_RECORD_FLAG_AUTOREFRESH:0x0001

The peer record must be automatically refreshed any time an event for the record is raised.

### -field PEER_RECORD_FLAG_DELETED:0x0002

The peer record is marked for deletion but has not yet been physically removed from the local computer.

