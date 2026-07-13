---
UID: NS:iscsidsc.ISCSI_TARGET_PORTAL_INFOW
title: ISCSI_TARGET_PORTAL_INFOW (iscsidsc.h)
description: ISCSI_TARGET_PORTAL_INFO structure contains information about a target portal. (Unicode)
helpviewer_keywords: ["*PISCSI_TARGET_PORTAL_INFOW","ISCSI_TARGET_PORTAL_INFO","ISCSI_TARGET_PORTAL_INFO structure [iSCSI Discovery Library API]","ISCSI_TARGET_PORTAL_INFOA","ISCSI_TARGET_PORTAL_INFOW","PISCSI_TARGET_PORTAL_INFO","PISCSI_TARGET_PORTAL_INFO structure pointer [iSCSI Discovery Library API]","iscsidisc.iscsi_target_portal_info","iscsidsc/ISCSI_TARGET_PORTAL_INFO","iscsidsc/ISCSI_TARGET_PORTAL_INFOA","iscsidsc/ISCSI_TARGET_PORTAL_INFOW","iscsidsc/PISCSI_TARGET_PORTAL_INFO"]
old-location: iscsidisc\iscsi_target_portal_info.htm
tech.root: iSCSIDisc
ms.assetid: 3592b289-9c0d-43dc-918f-23c8ff079186
ms.date: 12/05/2018
ms.keywords: '*PISCSI_TARGET_PORTAL_INFOW, ISCSI_TARGET_PORTAL_INFO, ISCSI_TARGET_PORTAL_INFO structure [iSCSI Discovery Library API], ISCSI_TARGET_PORTAL_INFOA, ISCSI_TARGET_PORTAL_INFOW, PISCSI_TARGET_PORTAL_INFO, PISCSI_TARGET_PORTAL_INFO structure pointer [iSCSI Discovery Library API], iscsidisc.iscsi_target_portal_info, iscsidsc/ISCSI_TARGET_PORTAL_INFO, iscsidsc/ISCSI_TARGET_PORTAL_INFOA, iscsidsc/ISCSI_TARGET_PORTAL_INFOW, iscsidsc/PISCSI_TARGET_PORTAL_INFO'
req.header: iscsidsc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ISCSI_TARGET_PORTAL_INFOW (Unicode) and ISCSI_TARGET_PORTAL_INFOA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: ISCSI_TARGET_PORTAL_INFOW, *PISCSI_TARGET_PORTAL_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PISCSI_TARGET_PORTAL_INFOW
 - iscsidsc/PISCSI_TARGET_PORTAL_INFOW
 - ISCSI_TARGET_PORTAL_INFOW
 - iscsidsc/ISCSI_TARGET_PORTAL_INFOW
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
 - ISCSI_TARGET_PORTAL_INFO
 - ISCSI_TARGET_PORTAL_INFOA
 - ISCSI_TARGET_PORTAL_INFOW
---

# ISCSI_TARGET_PORTAL_INFOW structure


## -description

The <b>ISCSI_TARGET_PORTAL_INFO</b> structure contains information about a target portal.

## -struct-fields

### -field InitiatorName

A string representing the name of the Host-Bus Adapter initiator.

### -field InitiatorPortNumber

The port number on the Host-Bus Adapter (HBA) associated with the portal. This port number corresponds to the source IP address on the HBA

### -field SymbolicName

A string representing the symbolic name of the portal.

### -field Address

A string representing the IP address or DNS name of the portal.

### -field Socket

The socket number.

## -remarks

> [!NOTE]
> The iscsidsc.h header defines ISCSI_TARGET_PORTAL_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

