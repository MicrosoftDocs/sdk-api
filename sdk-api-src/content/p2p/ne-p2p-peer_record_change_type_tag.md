---
UID: NE:p2p.peer_record_change_type_tag
title: peer_record_change_type_tag
author: windows-sdk-content
description: The PEER_RECORD_CHANGE_TYPE enumeration specifies the changes that can occur to a record.
old-location: p2p\peer_record_change_type.htm
old-project: P2PSdk
ms.assetid: d2451b45-eb42-4401-ab1d-505a41e25822
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PEER_RECORD_ADDED, PEER_RECORD_CHANGE_TYPE, PEER_RECORD_CHANGE_TYPE enumeration [Peer Networking], PEER_RECORD_DELETED, PEER_RECORD_EXPIRED, PEER_RECORD_UPDATED, p2p.peer_record_change_type, p2p/ PEER_RECORD_CHANGE_TYPE, p2p/PEER_RECORD_ADDED, p2p/PEER_RECORD_DELETED, p2p/PEER_RECORD_EXPIRED, p2p/PEER_RECORD_UPDATED, peer_record_change_type_tag
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
req.typenames: PEER_RECORD_CHANGE_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	P2P.h
api_name:
-	PEER_RECORD_CHANGE_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# peer_record_change_type_tag enumeration


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




<a href="https://msdn.microsoft.com/01404fff-3488-43aa-bc59-3e08ff925ea5">
        PEER_EVENT_RECORD_CHANGE_DATA</a>



<a href="https://msdn.microsoft.com/454b40f6-a7de-4b59-ae35-a809c4510133">
        PFNPEER_SECURE_RECORD</a>



<a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">
        PFNPEER_VALIDATE_RECORD</a>
 

 

