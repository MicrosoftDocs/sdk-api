---
UID: NS:iscsidsc.ISCSI_SESSION_INFOA
title: ISCSI_SESSION_INFOA (iscsidsc.h)
description: ISCSI_SESSION_INFO. (ANSI)
helpviewer_keywords: ["*PISCSI_SESSION_INFOA","ISCSI_SESSION_INFO","ISCSI_SESSION_INFO structure [iSCSI Discovery Library API]","ISCSI_SESSION_INFOA","ISCSI_SESSION_INFOW","PISCSI_SESSION_INFO","PISCSI_SESSION_INFO structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_session_info","iscsidsc/ISCSI_SESSION_INFO","iscsidsc/ISCSI_SESSION_INFOA","iscsidsc/ISCSI_SESSION_INFOW","iscsidsc/PISCSI_SESSION_INFO"]
old-location: iscsidisc\iscsi_session_info.htm
tech.root: iSCSIDisc
ms.assetid: 5da4aa28-a630-41f2-abb2-5538c11242e6
ms.date: 12/05/2018
ms.keywords: '*PISCSI_SESSION_INFOA, ISCSI_SESSION_INFO, ISCSI_SESSION_INFO structure [iSCSI Discovery Library API], ISCSI_SESSION_INFOA, ISCSI_SESSION_INFOW, PISCSI_SESSION_INFO, PISCSI_SESSION_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_session_info, iscsidsc/ISCSI_SESSION_INFO, iscsidsc/ISCSI_SESSION_INFOA, iscsidsc/ISCSI_SESSION_INFOW, iscsidsc/PISCSI_SESSION_INFO'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_SESSION_INFOW (Unicode) and ISCSI_SESSION_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ISCSI_SESSION_INFOA, *PISCSI_SESSION_INFOA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_SESSION_INFOA
 - iscsidsc/PISCSI_SESSION_INFOA
 - ISCSI_SESSION_INFOA
 - iscsidsc/ISCSI_SESSION_INFOA
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
 - ISCSI_SESSION_INFO
 - ISCSI_SESSION_INFOA
 - ISCSI_SESSION_INFOW
---

# ISCSI_SESSION_INFOA structure


## -description

The <b>ISCSI_SESSION_INFO</b> structure contains session information.

## -struct-fields

### -field SessionId

A <a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a> structure containing a unique identifier that represents the session.

### -field InitiatorName

A string that represents the initiator name.

### -field TargetNodeName

A string that represents the target node name.

### -field TargetName

A string that represents the target name.

### -field ISID

The initiator-side identifier (ISID) used in the iSCSI protocol.

### -field TSID

The target-side identifier (TSID) used in the iSCSI protocol.

### -field ConnectionCount

The number of connections associated with the session.

### -field Connections

A pointer to a <a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_connection_infoa">ISCSI_CONNECTION_INFO</a> structure.

## -see-also

<a href="/previous-versions/windows/desktop/api/iscsidsc/nf-iscsidsc-getiscsisessionlista">GetIScsiSessionList</a>



<a href="/previous-versions/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_connection_infoa">ISCSI_CONNECTION_INFO</a>



<a href="/windows/desktop/api/iscsidsc/ns-iscsidsc-iscsi_unique_session_id">ISCSI_UNIQUE_SESSION_ID</a>

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ISCSI_SESSION_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

