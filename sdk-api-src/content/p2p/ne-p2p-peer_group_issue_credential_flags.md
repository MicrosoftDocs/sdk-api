---
UID: NE:p2p.peer_issue_credential_flags_tag
title: PEER_GROUP_ISSUE_CREDENTIAL_FLAGS (p2p.h)
description: .
helpviewer_keywords: ["PEER_GROUP_ISSUE_CREDENTIAL_FLAGS","PEER_GROUP_ISSUE_CREDENTIAL_FLAGS enumeration [Peer Networking]","PEER_GROUP_STORE_CREDENTIALS","p2p.peer_group_issue_credential_flags","p2p/PEER_GROUP_ISSUE_CREDENTIAL_FLAGS","p2p/PEER_GROUP_STORE_CREDENTIALS"]
old-location: p2p\peer_group_issue_credential_flags.htm
tech.root: p2p
ms.assetid: b5397627-ffd7-453c-b829-e3e04fa9894a
ms.date: 12/05/2018
ms.keywords: PEER_GROUP_ISSUE_CREDENTIAL_FLAGS, PEER_GROUP_ISSUE_CREDENTIAL_FLAGS enumeration [Peer Networking], PEER_GROUP_STORE_CREDENTIALS, p2p.peer_group_issue_credential_flags, p2p/PEER_GROUP_ISSUE_CREDENTIAL_FLAGS, p2p/PEER_GROUP_STORE_CREDENTIALS
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
req.typenames: PEER_GROUP_ISSUE_CREDENTIAL_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_issue_credential_flags_tag
 - p2p/peer_issue_credential_flags_tag
 - PEER_GROUP_ISSUE_CREDENTIAL_FLAGS
 - p2p/PEER_GROUP_ISSUE_CREDENTIAL_FLAGS
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
 - PEER_GROUP_ISSUE_CREDENTIAL_FLAGS
---

# PEER_GROUP_ISSUE_CREDENTIAL_FLAGS enumeration


## -description

The <b>PEER_GROUP_ISSUE_CREDENTIAL_FLAGS</b> are used to specify if user credentials are stored within a group.

## -enum-fields

### -field PEER_GROUP_STORE_CREDENTIALS:0x0001

When the <b>PEER_GROUP_STORE_CREDENTIALS</b> flag is set, the user  credentials are stored within a group database to be retrieved when the user connects. If the flag is not set, any new credentials are returned in string form and must be passed to the user out-of-band.

