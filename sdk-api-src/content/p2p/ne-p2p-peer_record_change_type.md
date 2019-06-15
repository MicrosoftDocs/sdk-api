---
UID: NE:p2p.peer_record_change_type_tag
title: PEER_RECORD_CHANGE_TYPE (p2p.h)
author: windows-sdk-content
description: The PEER_RECORD_CHANGE_TYPE enumeration specifies the changes that can occur to a record.
old-location: p2p\peer_record_change_type.htm
tech.root: P2PSdk
ms.assetid: d2451b45-eb42-4401-ab1d-505a41e25822
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PEER_RECORD_ADDED, PEER_RECORD_CHANGE_TYPE, PEER_RECORD_CHANGE_TYPE enumeration [Peer Networking], PEER_RECORD_DELETED, PEER_RECORD_EXPIRED, PEER_RECORD_UPDATED, p2p.peer_record_change_type, p2p/PEER_RECORD_ADDED, p2p/PEER_RECORD_CHANGE_TYPE, p2p/PEER_RECORD_DELETED, p2p/PEER_RECORD_EXPIRED, p2p/PEER_RECORD_UPDATED
ms.topic: enum
f1_keywords: ["p2p/PEER_RECORD_CHANGE_TYPE"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_RECORD_CHANGE_TYPE
product: Windows
targetos: Windows
req.typenames: PEER_RECORD_CHANGE_TYPE
req.redist: 
ms.custom: 19H1
---

# PEER_RECORD_CHANGE_TYPE enumeration


## -description


The <b>PEER_RECORD_CHANGE_TYPE</b> enumeration specifies the changes that can occur to a record.


## -enum-fields




### -field PEER_RECORD_ADDED

Indicates that the specified record is added to the peer graph or group.


### -field PEER_RECORD_UPDATED

Indicates that the specified record is updated in the peer graph or group.


### -field PEER_RECORD_DELETED

Indicates that the specified record is deleted from the peer graph or group.


### -field PEER_RECORD_EXPIRED

Indicates that the specified record is expired and removed from the peer graph or group.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/ns-p2p-peer_event_record_change_data_tag">PEER_EVENT_RECORD_CHANGE_DATA</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nc-p2p-pfnpeer_secure_record">PFNPEER_SECURE_RECORD</a>



<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nc-p2p-pfnpeer_validate_record">PFNPEER_VALIDATE_RECORD</a>
 

 

