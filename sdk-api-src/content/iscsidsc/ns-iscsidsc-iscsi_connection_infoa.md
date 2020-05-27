---
UID: NS:iscsidsc.__unnamed_struct_16
title: ISCSI_CONNECTION_INFOA (iscsidsc.h)
description: ISCSI_CONNECTION_INFO structure contains information about a connection.
helpviewer_keywords: ["*PISCSI_CONNECTION_INFOA","ISCSI_CONNECTION_INFO","ISCSI_CONNECTION_INFO structure [iSCSI Discovery Library API]","ISCSI_CONNECTION_INFOA","ISCSI_CONNECTION_INFOW","PISCSI_CONNECTION_INFO","PISCSI_CONNECTION_INFO structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_connection_info","iscsidsc/ISCSI_CONNECTION_INFO","iscsidsc/ISCSI_CONNECTION_INFOA","iscsidsc/ISCSI_CONNECTION_INFOW","iscsidsc/PISCSI_CONNECTION_INFO"]
old-location: iscsidisc\iscsi_connection_info.htm
tech.root: iSCSIDisc
ms.assetid: 4bfe2f36-2e68-4093-9660-b0140baeea80
ms.date: 12/05/2018
ms.keywords: '*PISCSI_CONNECTION_INFOA, ISCSI_CONNECTION_INFO, ISCSI_CONNECTION_INFO structure [iSCSI Discovery Library API], ISCSI_CONNECTION_INFOA, ISCSI_CONNECTION_INFOW, PISCSI_CONNECTION_INFO, PISCSI_CONNECTION_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_connection_info, iscsidsc/ISCSI_CONNECTION_INFO, iscsidsc/ISCSI_CONNECTION_INFOA, iscsidsc/ISCSI_CONNECTION_INFOW, iscsidsc/PISCSI_CONNECTION_INFO'
f1_keywords:
- iscsidsc/ISCSI_CONNECTION_INFO
dev_langs:
- c++
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_CONNECTION_INFOW (Unicode) and ISCSI_CONNECTION_INFOA (ANSI)
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
- Iscsidsc.h
api_name:
- ISCSI_CONNECTION_INFO
- ISCSI_CONNECTION_INFOA
- ISCSI_CONNECTION_INFOW
targetos: Windows
req.typenames: ISCSI_CONNECTION_INFOA, *PISCSI_CONNECTION_INFOA
req.redist: 
ms.custom: 19H1
---

# ISCSI_CONNECTION_INFOA structure


## -description


The 	<b>ISCSI_CONNECTION_INFO</b> structure contains information about a connection.


## -struct-fields




### -field ConnectionId

A ISCSI_UNIQUE_CONNECTION_ID structure that contains the unique identifier for a connection. The LoginIScsiTarget and AddIScsiConnection functions return this value via the UniqueConnectionId parameter.


### -field InitiatorAddress

A string that represents the IP address of the initiator.


### -field TargetAddress

A string that represents the IP address of the target.


### -field InitiatorSocket

The socket number on the initiator that establishes the connection.


### -field TargetSocket

The socket number on the target that establishes the connection.


### -field CID

The connection identifier for the connection.


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/legacy/bb870817(v=vs.85)">ISCSI_UNIQUE_CONNECTION_ID</a>
 

 

