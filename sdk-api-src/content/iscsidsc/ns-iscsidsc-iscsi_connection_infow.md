---
UID: NS:iscsidsc.ISCSI_CONNECTION_INFOW
title: ISCSI_CONNECTION_INFOW (iscsidsc.h)
description: ISCSI_CONNECTION_INFO structure contains information about a connection. (Unicode)
helpviewer_keywords: ["*PISCSI_CONNECTION_INFOW","ISCSI_CONNECTION_INFO","ISCSI_CONNECTION_INFO structure [iSCSI Discovery Library API]","ISCSI_CONNECTION_INFOA","ISCSI_CONNECTION_INFOW","PISCSI_CONNECTION_INFO","PISCSI_CONNECTION_INFO structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_connection_info","iscsidsc/ISCSI_CONNECTION_INFO","iscsidsc/ISCSI_CONNECTION_INFOA","iscsidsc/ISCSI_CONNECTION_INFOW","iscsidsc/PISCSI_CONNECTION_INFO"]
old-location: iscsidisc\iscsi_connection_info.htm
tech.root: iSCSIDisc
ms.assetid: 4bfe2f36-2e68-4093-9660-b0140baeea80
ms.date: 12/05/2018
ms.keywords: '*PISCSI_CONNECTION_INFOW, ISCSI_CONNECTION_INFO, ISCSI_CONNECTION_INFO structure [iSCSI Discovery Library API], ISCSI_CONNECTION_INFOA, ISCSI_CONNECTION_INFOW, PISCSI_CONNECTION_INFO, PISCSI_CONNECTION_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_connection_info, iscsidsc/ISCSI_CONNECTION_INFO, iscsidsc/ISCSI_CONNECTION_INFOA, iscsidsc/ISCSI_CONNECTION_INFOW, iscsidsc/PISCSI_CONNECTION_INFO'
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
targetos: Windows
req.typenames: ISCSI_CONNECTION_INFOW, *PISCSI_CONNECTION_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_CONNECTION_INFOW
 - iscsidsc/PISCSI_CONNECTION_INFOW
 - ISCSI_CONNECTION_INFOW
 - iscsidsc/ISCSI_CONNECTION_INFOW
dev_langs:
 - c++
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

<a href="/previous-versions/windows/desktop/legacy/bb870817(v=vs.85)">ISCSI_UNIQUE_CONNECTION_ID</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ISCSI_CONNECTION_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

