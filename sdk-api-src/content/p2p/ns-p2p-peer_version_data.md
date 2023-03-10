---
UID: NS:p2p.peer_version_data_tag
title: PEER_VERSION_DATA (p2p.h)
description: The PEER_VERSION_DATA structure contains the version information about the Peer Graphing and Grouping APIs.
helpviewer_keywords: ["*PPEER_VERSION_DATA","PEER_VERSION_DATA","PEER_VERSION_DATA structure [Peer Networking]","PPEER_VERSION_DATA","PPEER_VERSION_DATA structure pointer [Peer Networking]","p2p.peer_version_data","p2p/PPEER_VERSION_DATA","p2p/peer_version_data_tag"]
old-location: p2p\peer_version_data.htm
tech.root: p2p
ms.assetid: b212101f-8c34-41d1-92b9-4daf3591200e
ms.date: 12/05/2018
ms.keywords: '*PPEER_VERSION_DATA, PEER_VERSION_DATA, PEER_VERSION_DATA structure [Peer Networking], PPEER_VERSION_DATA, PPEER_VERSION_DATA structure pointer [Peer Networking], p2p.peer_version_data, p2p/PPEER_VERSION_DATA, p2p/peer_version_data_tag'
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
req.typenames: PEER_VERSION_DATA, *PPEER_VERSION_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_version_data_tag
 - p2p/peer_version_data_tag
 - PPEER_VERSION_DATA
 - p2p/PPEER_VERSION_DATA
 - PEER_VERSION_DATA
 - p2p/PEER_VERSION_DATA
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
 - PEER_VERSION_DATA
---

# PEER_VERSION_DATA structure


## -description

The <b>PEER_VERSION_DATA</b> structure contains the version information about the Peer Graphing and Grouping APIs.

## -struct-fields

### -field wVersion

Specifies the version of the Peer Infrastructure for a caller to use. The version to use is based on the Peer Infrastructure DLL installed on a local computer.  A high order-byte specifies the minor version (revision) number.  A low-order byte specifies the major version number.

### -field wHighestVersion

Specifies the highest version of the Peer Infrastructure that the Peer DLL installed on the local computer can support. Typically, this value is the same as <b>wVersion</b>.

## -see-also

<a href="/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peergroupstartup">PeerGroupStartup</a>