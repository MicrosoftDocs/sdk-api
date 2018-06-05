---
UID: NE:p2p.peer_record_flags_tag
title: peer_record_flags_tag
author: windows-sdk-content
description: The PEER_RECORD_FLAGS enumeration specifies a set of flags for peer record behaviors.
old-location: p2p\peer_record_flags.htm
old-project: P2PSdk
ms.assetid: 2ae2411d-3409-442a-8655-e54a34bf3938
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PEER_RECORD_FLAGS, PEER_RECORD_FLAGS enumeration [Peer Networking], PEER_RECORD_FLAG_AUTOREFRESH, PEER_RECORD_FLAG_DELETED, p2p.peer_record_flags, p2p/PEER_RECORD_FLAGS, p2p/PEER_RECORD_FLAG_AUTOREFRESH, p2p/PEER_RECORD_FLAG_DELETED, peer_record_flags_tag
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: PEER_RECORD_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_RECORD_FLAGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_record_flags_tag enumeration


## -description



      The <b>PEER_RECORD_FLAGS</b> enumeration specifies a set of flags for peer record behaviors.


## -enum-fields




### -field PEER_RECORD_FLAG_AUTOREFRESH

The peer record must be automatically refreshed any time an event for the record is raised.


### -field PEER_RECORD_FLAG_DELETED

The peer record is marked for deletion but has not yet been physically removed from the local computer.

