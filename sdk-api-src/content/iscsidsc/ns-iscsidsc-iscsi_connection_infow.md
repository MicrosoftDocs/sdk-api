---
UID: NS:iscsidsc.ISCSI_CONNECTION_INFOW
title: ISCSI_CONNECTION_INFOW
author: windows-sdk-content
description: ISCSI_CONNECTION_INFO structure contains information about a connection.
old-location: iscsidisc\iscsi_connection_info.htm
tech.root: iSCSIDisc
ms.assetid: 4bfe2f36-2e68-4093-9660-b0140baeea80
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PISCSI_CONNECTION_INFOW, ISCSI_CONNECTION_INFO, ISCSI_CONNECTION_INFO structure [iSCSI Discovery Library API], ISCSI_CONNECTION_INFOA, ISCSI_CONNECTION_INFOW, PISCSI_CONNECTION_INFO, PISCSI_CONNECTION_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_connection_info, iscsidsc/ISCSI_CONNECTION_INFO, iscsidsc/ISCSI_CONNECTION_INFOA, iscsidsc/ISCSI_CONNECTION_INFOW, iscsidsc/PISCSI_CONNECTION_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: ISCSI_CONNECTION_INFOW, *PISCSI_CONNECTION_INFOW
req.redist: 
---

# ISCSI_CONNECTION_INFOW structure


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




<a href="https://msdn.microsoft.com/cc68fda4-6dbf-42de-8e0e-e144bd4e9524">ISCSI_UNIQUE_CONNECTION_ID</a>
 

 

