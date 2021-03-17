---
UID: NS:p2p.peer_data_tag
title: PEER_DATA (p2p.h)
description: The PEER_DATA structure contains binary data.
helpviewer_keywords: ["*PPEER_DATA","PEER_DATA","PEER_DATA structure [Peer Networking]","PPEER_DATA","PPEER_DATA structure pointer [Peer Networking]","p2p.peer_data","p2p/PPEER_DATA","p2p/peer_data_tag"]
old-location: p2p\peer_data.htm
tech.root: p2p
ms.assetid: d8a8b9e3-c455-4813-b812-263efe7f5e3e
ms.date: 12/05/2018
ms.keywords: '*PPEER_DATA, PEER_DATA, PEER_DATA structure [Peer Networking], PPEER_DATA, PPEER_DATA structure pointer [Peer Networking], p2p.peer_data, p2p/PPEER_DATA, p2p/peer_data_tag'
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
req.typenames: PEER_DATA, *PPEER_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_data_tag
 - p2p/peer_data_tag
 - PPEER_DATA
 - p2p/PPEER_DATA
 - PEER_DATA
 - p2p/PEER_DATA
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
 - PEER_DATA
---

# PEER_DATA structure


## -description

The <b>PEER_DATA</b> structure contains binary data.

## -struct-fields

### -field cbData

Size of  <b>pbData</b>, in bytes. It is possible for this value to be set to zero if <b>pbData</b> contains no data.

### -field pbData

Pointer to a buffer.

### -field pbData.size_is

### -field pbData.size_is.cbData

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_event_incoming_data">PEER_EVENT_INCOMING_DATA</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_record">PEER_RECORD</a>



<a href="/windows/desktop/api/p2p/nc-p2p-pfnpeer_free_security_data">PFNPEER_FREE_SECURITY_DATA</a>



<a href="/windows/desktop/api/p2p/nc-p2p-pfnpeer_secure_record">PFNPEER_SECURE_RECORD</a>